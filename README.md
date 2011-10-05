# Disqus Nagios plugins

This is a collection of Nagios plugins written at Disqus.

## Scripts

* check_graphite.rb

## check_graphite.rb

     % ./check_graphite.rb -h
     Usage: ./check_graphite.rb [options]
         -U, --graphite-url [URL]         Query Graphite on URL (default: http://localhost/)
         -t, --targets [TARGET1|TARGET2]  Show metrics for TARGET1, TARGET2
             --from TIME                  Set start time to TIME
             --until [TIME]               Set end time to TIME (default: now)
             --percent [PCT]              Set percent threshold to PCT 
             --threshold [VAL]            set hard threshold to VAL 
             --over                       Alert on values over threshold (default: false)
             --under                      Alert on values under threshold (default: true)
         -W [NUM]                         Warn on NUM values beyond threshold (default: 0)
         -C [NUM]                         Critical on NUM values beyond threshold (default: 0)
         -u, --auth-user [USER]           Username for http auth
         -p, --auth-password [PASSWORD]   Password for http auth

Mandatory arguments: -U, -t, --from, [--percent|--threshold]

Separate multiple targets with "|". (obviously) use quotes so the shell doesn't interpret the pipe.
