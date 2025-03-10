## Release summary

This is a minor release that 
 
 Adds or creates aliases for the following NCAA baseball functions:
    - ncaa_teams()
    - load_ncaa_baseball_pbp()
    - load_ncaa_baseball_teams()
    - load_ncaa_baseball_season_ids()
    - load_ncaa_baseball_schedule()
    - ncaa_pbp() (see aliasing below)
    - ncaa_roster() (see aliasing below)
    - ncaa_team_player_stats() (see aliasing below)
  
 Makes the following parameter changes:
 
 * ncaa_*() functions now return team_id and team_name instead of school_id and school
 * Add proxy rlang dots option for passing httr::use_proxy() option to ncaa_*() functions
 * ncaa_lineups() function removes the year parameter (was unnecessary)
 * ncaa_*() functions now uniformly use team_id instead of teamid, year (vs. team_year). This affects the following functions
   - ncaa_roster()
   - ncaa_schedule_info()
   - ncaa_park_factor()
   - ncaa_team_player_stats()
   
 Aliases the following functions:
 
 * ncaa_baseball_pbp() has been aliased to ncaa_pbp() for naming consistency
 * ncaa_baseball_roster() has been aliased to ncaa_roster() for naming consistency
 * ncaa_scrape() has been aliased to ncaa_team_player_stats() for more descriptive naming
 
 Makes these other fixes: 
 
* Under the hood fixes for mlb_venues(), fg_team_batter(), fg_team_pitcher(),
  fg_batter_leaders(), fg_pitcher_leaders(), chadwick_player_lu()
* Updates for tidyselect deprecation of data masking for related dplyr and tidyr functions
* Also resolves the issue cited with vignette by CRAN maintainers
* Unwraps several examples for testing purposes. I will not unwrap more because they connect to 
  outside internet resources. This can have adverse affects on the API's accessed. 
  Our own testing is automated via GitHub Actions and is extensive enough that I feel confident 
  we will catch errors in a sufficiently quick fashion. I simply am not interested in an API 
  resource being temporarily down or misfiring triggering a CRAN alert for me. Everything in the 
  package connects to the internet, so I try to be polite on giving examples that will be repeatedly
  called. 

## R CMD check results

0 errors | 0 warnings | 0 notes

## revdepcheck results

We checked 0 reverse dependencies, comparing R CMD check results across CRAN and dev versions of this package.

 * We saw 0 new problems
 * We failed to check 0 packages
