# github-repo-compare

A command line tool you can use to compare a list of git repos by stars, watchers, forks, issues.
You can use this tool to help you decide which library to use in your project based on its popularity.
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
- replace the contents of repos.txt with the list of repositories you'd like to compare

## Usage

- cd to the cloned git directory and run: `./github-repo-compare`

## Example report (generated 12/07/2017)

I was trying to decide which command line argument parser library to use for a golang command line tool and I found a [list on awesome-go](https://github.com/avelino/awesome-go#command-line). I wasn't sure which one to choose so I wrote this utility.

```bash
name                 stars      watchers   forks      issues     
-------------------- ---------- ---------- ---------- ---------- 
urfave/cli                 7016        198        636         81 
spf13/cobra                5835        159        485         75 
odeke-em/drive             3714        188        293        190 
alecthomas/kingpin         1603         38        113         13 
chzyer/readline            1027         34         89         36 
jessevdk/go-flags           925         25        122         19 
docopt/docopt.go            873         32         70         24 
tcnksm/gcli                 765         26         65         18 
mitchellh/cli               704         22         56          9 
jawher/mow.cli              470         20         33          6 
alexflint/go-arg            450         15         21          1 
peterh/liner                411         19         65          2 
posener/complete            389         11         17          1 
mkideal/cli                 320         15         24         15 
spf13/pflag                 284         17         98         16 
tucnak/climax               126          7         11          4 
ukautz/clif                  79          2          9          5 
cosiner/flag                 72          4          2          4 
octago/sflags                44          5          3          3 
dixonwille/wmenu             37          0          4          1 
dixonwille/wlog              22          0          2          0 
teris-io/cli                 18          1          0          0 
codingconcepts/env            9          1          1          0 
akamensky/argparse            5          0          0          5 
cosiner/argv                  3          1          0          0 
```

## Notes

You need a github token because of rate limiting for the github api.