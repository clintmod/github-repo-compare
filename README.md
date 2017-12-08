# github-repo-compare

A command line tool you can use to compare a list of git repos by stars,
watchers, forks, issues, created date, last commit date to master.
You can use this tool to help you decide which library to use in
your project based on its popularity.
It outputs the list on the command line sorted by stars.
It also writes the report to a file called stats.txt

## Setup

- get a [github personal token](https://github.com/settings/tokens/)
- setup the environment variables (nix example below... on win use `set` instead)

```bash
export GITHUB_REPO_COMPARE_TOKEN=[YOUR PERSONAL GITHUB TOKEN]
export GITHUB_REPO_COMPARE_USERNAME=[YOUR GITHUB USERNAME]

```

- clone this git repository to your local machine
- cd to the newly cloned repo
- replace the contents of `repos.txt` with the list of repositories you'd like to compare

## Usage

- cd to the cloned git directory and run: `./github-repo-compare`

## Example report (generated 12/07/2017)

I was trying to decide which command line argument parser library to use for a golang command line tool.
I found a [list on awesome-go](https://github.com/avelino/awesome-go#command-line). 
I wasn't sure which one to choose so I wrote this utility.

```bash
name                           stars      watchers   forks      issues     created               last commit (master)  
------------------------------ ---------- ---------- ---------- ---------- --------------------- --------------------- 
urfave/cli                           7018        198        635         81 2013-07-13T19:32:06Z  2017-12-03T21:42:37Z  
spf13/cobra                          5846        160        487         75 2013-09-03T20:40:26Z  2017-12-07T07:49:35Z  
odeke-em/drive                       3717        188        294        190 2014-11-03T08:18:11Z  2017-10-09T01:47:46Z  
alecthomas/kingpin                   1604         38        113         13 2014-05-14T20:09:04Z  2017-11-27T20:08:19Z  
chzyer/readline                      1027         34         89         34 2015-09-20T15:11:30Z  2017-12-08T01:17:16Z  
jessevdk/go-flags                     925         25        123         19 2012-08-31T13:57:58Z  2017-09-26T14:47:05Z  
docopt/docopt.go                      873         32         70         24 2013-08-25T23:05:52Z  2016-02-16T23:20:12Z  
tcnksm/gcli                           764         26         65         18 2014-06-19T09:10:15Z  2017-01-29T03:38:39Z  
mitchellh/cli                         704         22         56          9 2013-11-03T06:47:54Z  2017-11-29T19:36:17Z  
jawher/mow.cli                        470         20         33          6 2014-12-18T19:34:20Z  2017-11-11T12:18:41Z  
alexflint/go-arg                      450         15         21          1 2015-11-01T01:30:06Z  2017-10-03T00:07:17Z  
peterh/liner                          411         19         65          2 2012-08-15T16:34:55Z  2017-11-22T03:03:39Z  
posener/complete                      389         11         17          1 2017-05-05T21:34:07Z  2017-11-04T09:57:02Z  
mkideal/cli                           321         15         24         15 2016-02-26T16:45:29Z  2017-03-24T15:56:50Z  
spf13/pflag                           285         17         98         16 2013-08-30T14:53:31Z  2017-11-06T14:28:49Z  
tucnak/climax                         126          7         11          4 2015-11-03T21:04:57Z  2016-01-10T10:13:00Z  
ukautz/clif                            79          2          9          5 2015-05-30T18:30:08Z  2015-06-17T07:34:47Z  
cosiner/flag                           72          4          2          4 2016-10-05T16:49:41Z  2017-07-16T09:01:35Z  
octago/sflags                          44          5          3          3 2016-12-04T14:49:27Z  2017-05-28T18:17:28Z  
dixonwille/wmenu                       37          0          4          1 2016-04-20T13:09:44Z  2017-07-21T00:05:58Z  
dixonwille/wlog                        22          0          2          0 2016-04-13T16:47:40Z  2017-07-20T23:52:29Z  
teris-io/cli                           18          1          0          0 2017-05-24T23:07:07Z  2017-10-29T15:38:18Z  
codingconcepts/env                      9          1          1          0 2017-06-14T20:01:55Z  2017-10-05T08:04:04Z  
akamensky/argparse                      5          0          0          6 2017-11-24T06:42:20Z  2017-12-07T06:17:44Z  
cosiner/argv                            3          1          0          0 2017-01-22T10:37:21Z  2017-02-25T14:54:30Z
```

## Notes

You need a github token because of rate limiting for the github api.