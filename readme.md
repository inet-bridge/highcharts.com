#Highcharts JS
Highcharts JS is a JavaScript charting library based on SVG and VML rendering.

* Official website:  [www.highcharts.com](http://www.highcharts.com)
* Official download: [www.highcharts.com/download](http://www.highcharts.com/download)
* Licensing: [www.highcharts.com/license](http://www.highcharts.com/license)
* Support: [www.highcharts.com/support](http://www.highcharts.com/support)

## Current branches
**master**: As of 2013-03-06, the master branch holds the candidate for Highcharts 3.0 and Highstock 1.3.

**rambera**: This branch contained the candidate for Highcharts 3.0 and Highstock 1.3 until 2013-03-16. After this date, this branch is abandoned and work will continue on the master branch.

## Reporting issues
We use GitHub Issues as our official bug tracker. We strive to keep this a clean, maintainable and searchable record of our open and closed bugs, therefore we kindly ask you to obey some rules before reporting an issue:

1. Make sure the report is accompanied by a reproducible demo. The ideal demo is created by forking [our standard jsFiddle](http://jsfiddle.net/highcharts/llexl/), adding your own code and stripping it down to an absolute minimum needed to demonstrate the bug.
* Always add information on what browser it applies to, and other information needed for us to debug.
* It may be that the bug is already fixed. Try your chart with our latest work from http://github.highcharts.com/master/highcharts.js before reporting.
* For feature requests, tech support and general discussion, don't use GitHub Issues. See [www.highcharts.com/support](www.highcharts.com/support) for the appropriate channels.

## I-Net Bridge

The forked versions are in branches prefixed with `inet_`, such as `inet_highstock_v1.2.5`.

Building a new fork:

1. Pull upstream changes, along with tags, eg. `git pull upstream --tags` (where upstream is the name of the remote pointing to the original Highcharts repo).
1. Check out the tag of the release you wish to fork, eg. `git checkout highstock-v1.3.2`.
1. Switch to a new branch, eg. `git checkout -b inet_highstock_v1.3.2`.
1. Check which current patches are still necessary. Apply them as separate commits.
1. Add any new patches. Make sure to commit each patch separately, so they are easy to apply selectively next time.
1. Run `ant dist` from the command line to build the new Highcharts version. Building Highcharts is explained in detail in the [build file](build.md).
1. Push the new branch and make it the default on Github.
1. Include build/dist/highstock/js/highstock.src.js and build/dist/highstock/js/modules/exporting.src.js to the project's vendor libs and rename them highstock.js and exporting.js, respectively.
