date-svcs
=========

An NPM module providing a set of date/time utilities.

Installing
----------

    npm install date-svcs

Using
-----

    const dateSVC = require('date-svcs')
    const moment = require('moment')

    # Note that when the 'current date' is expected, the current
    # date will be defines as in the America/Denver timezone.

    # Return the first day of the current month
    dateSVC.firstOfCurrentMonth()

    # Return the first date of the specified month
    dateSVC.firstOfCurrentMonth(moment('2015-03-10'))

    # Return the last date of the specified month
    dateSVC.lastOfCurrentMonth()

    # Return the last date of the specified month
    dateSVC.lastOfCurrentMonth(moment('2015-03-10'))

    # Return the day range for the current date
    dateSVC.dayRange()

    # Return the day range for the specified day
    dateSVC.dayRange(moment('2015-03-10'))

    # Return the range for the current month
    dateSVC.determineMonthRange()

    # Return the range for the month with the specified day
    dateSVC.determineMonthRange(moment('2015-03-10'))

    # Return the month ranges for the current day as far
    # back as the noEarlierThan date
    let noEarlierThan = moment('2015-12-03')
    dateSVC.determineDateRanges(noEarlierThan)

    # Return the month ranges for the specified date as far
    # back as the noEarlierThan date
    let noEarlierThan = moment('2015-12-03')
    dateSVC.determineDateRanges(noEarlierThan, moment('2016-02-12'))

    # Return the month ranges for the past three months
    dateSVC.pastThreeMonths()

    # Return the month ranges for the three months prior to the specified
    # date
    dateSVC.pastThreeMonths(moment('2016-01-12'))

    # Returns the past week's day ranges
    dateSVC.pastWeekRanges()

    # Returns the week's day ranges prior to the specified date
    dateSVC.pastWeekRanges(moment('2016-01-23')

    # Parses the date using the moment library
    dateSVC.parseDate('2014-01-01') # 2014-01-01T00:00:00.000Z

    # Returns today's date in the America/Denver timezone
    dateSVC.today() # '2016-05-16T17:10:32-06:00'

Copyright
=========

Copyright (c) 2016 Dave Sieh

See LICENSE.txt for details.
