# utcDayBoundary

A function that returns day boundary timestamps in UTC.

The boundary starts at the beginning of the indicated {day}, and ends
at the end of the indicated {day}. Boundary timestamps are returned in
UTC time.

Example:

    var utcDayBoundary = require('./utcDayBoundary');
    
    var boundaryObj = utcDayBoundary('2015-05-31T01:00:00.000Z', 'America/Los_Angeles');
    
    console.log(JSON.stringify(boundaryObj, null, 2));


    =>
    {
      "day": "2015-05-31T01:00:00.000Z",
      "tz": "America/Los_Angeles",
      "tzYear": 2015,
      "tzMonth": 5,
      "tzDay": 30,
      "tzTime": "18:00:00",
      "utcStart": "2015-05-30T07:00:00+00:00",
      "utcEnd": "2015-05-31T06:59:59+00:00"
    }
    
    
