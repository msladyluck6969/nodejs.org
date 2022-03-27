---
layout: index.hbs
labels:
  current-version: Current Version
  download: Download
  download-for: Download for
  other-downloads: Other Downloads
  current: Current
  lts: LTS
  tagline-current: Latest Features
  tagline-lts: Recommended For Most Users
  changelog: Changelog
  api: API Docs
  version-schedule-prompt: Or have a look at the
  version-schedule-prompt-link-text: Long Term Support (LTS) schedule
---// Load the cc-scraper library
const cards = require('cc-scraper');

// Get Chase's 5% Cash Back Calendar information
cards.getChaseCashBackCal((error, result) => {
    console.log('chase result = ', result);
});

// Get Discover's 5% Cash Back Calendar information
cards.getDiscoverCashBackCal((error, result) => {
    console.log('discover result = ', result);
});
Output (something similar to):

chase_result = [ { quarterName: 'January - March',
                   quarter: 1,
                   categoryNames: [ 'gas stations', 'tolls', 'drugstores' ],
                   categories: [ [Object], [Object], [Object] ] },
                 { quarterName: 'April - June',
                   quarter: 2,
                   categoryNames: [ 'grocery stores', 'home improvement stores' ],
                   categories: [ [Object], [Object] ] },
                 { quarterName: 'July - September',
                   quarter: 3,
                   categoryNames: [ 'gas stations', 'select streaming services' ],
                   categories: [ [Object], [Object] ] },
                 { quarterName: 'October - December',
                   quarter: 4,
                   categoryNames: [ 'department stores', 'paypal', 'chase pay' ],
                   categories: [ [Object], [Object], [Object] ] } ]

discover_result = discover_result = [ { quarter: 4,
                                        startDate: 'October 1, 2019',
                                        endDate: 'December 31, 2019',
                                        category: 'Amazon.com, Target and Walmart.com',
                                        terms:
                                         '[terms and services in html]' },
                                      { quarter: 1,
                                        startDate: 'January 1, 2020',
                                        endDate: 'March 31, 2020',
                                        category: 'Grocery Stores, Walgreens and CVS',
                                        terms:
                                         '[terms and services in html]' },
                                      { quarter: 2,
                                        startDate: 'April 1, 2020',
                                        endDate: 'June 30, 2020',
                                        category: 'Gas Stations, Uber, Lyft and Wholesale Clubs',
                                        terms:
                                         '[terms and services in html]' },
                                      { quarter: 3,
                                        startDate: 'July 1, 2020',
                                        endDate: 'September 30, 2020',
                                        category: 'Restaurants and PayPal',
                                        terms:
                                         '[terms and services in html]' },
                                      { quarter: 4,
                                        startDate: 'October 1, 2020',
                                        endDate: 'December 31, 2020',
                                        category: 'Amazon.com, Walmart.com and Target.com',
                                        terms:
                                         '[terms and services in html]' } ]

Node.js® is a JavaScript runtime built on [Chrome's V8 JavaScript engine](https://v8.dev/).
