Ember Redstone Project
======================

### Story and idea of this Project ###

### What is Ember.js? ###


### Where does the data come from? ###
The data is coming from the only source of truth - the production REDMINE database itself. It exposes a REST API which we can use to get *live* data, yes you are seeing this right, the data is live.

### Changelog ###

##### March 07 2016 #####
_EOD commit : 2a0a1c9_
- added readme.md
- figured model enumerables to parse through model data

##### March 04 2016 #####
_EOD commit : dffcdcf_
- updated to ember 2.4.0
- added journal as it's own model
- linking based on last commit works flawless
- introduced bug as I am looking for nested properties with @each to get my journals [test only pass as 55/61]
- started implementing project graph

##### March 02 2016 #####
_EOD commit : 4df0e4f_
- fixed dependencies
- fixed controller model setups
- updated today's tickets in mirage
- masonry layout for cards implemented
- dashboard and project pages transferred to masonry
- card template adapted to masonry
- adjusted masonry for Firefox
- journals have their own model

##### March 02 2016 #####
_EOD commit : c095f93_
- function now returning model results

##### March 01 2016 #####
_EOD commit : e3a9099_
- unused packages removed
- search-box component added
- search working and only dependent on controller now
- search-box pretty, needs a little fix
- updated some transition styles
- updated dashboard filter

##### February 29 2016 #####
_EOD commit : c155f46_
- found jsonp documentation
https://redmine.mozy.lab.emc.com//issues.json?limit=100&key=3b99b481e065d2de907ed09a1ec98b3826a05575&callback=redstone will do it // needs to be enabled by Tyler Peters

- overflow:hidden for cards
- added custom fields to issue model
- added custom field serializer

##### February 28 2016 #####
_EOD commit : f5a8bo5_
- added project serializer for parent relationship
- added parent attribute to project model
- projects template show parent project if it exists

- index controller knows about search
- changed issue controller to look for content instead of model to avoid confusion

##### February 27 2016 #####
_EOD commit : e3dde24_
- added card-component
- added card styles
- added font-awesome
- changed RedStone title to 'Redstone'
- did something about parsing the journals
- added some more animations for the cards
- did some change in 'about' template
- added card view to projects
- modified the really simple looking project view
- experiment further with search

- model manager for graph implemented
- navigation now looking pristine

##### February 25 2016 #####
_EOD commit : 3e3e0a9_
Dependencies added:
- ember-cli-filter-component
- ember-google-charts

- added journal support for issues

##### February 24 2016 #####
_EOD commit : b78b8dc_
- models adjusted to hold more object properties
- model relationship tests successful
- implemented REST Adapter
- using mirage for fixture data now
- ! Redmine API limitation - only returns 100 items; need to think about that another time
- ! Redmine doesn't support CORS header; yay - thanks Redmine!

- injected Skeleton CSS framework for grid bliss
- footer section now slightly less ugly
- header is pretty
- templating changed
- index route is now called dashboard
- issue & project requests are now returning a single promise
- dashboard performance doubled (rough estimate)

##### February 23 2016 #####
_EOD commit : ae60154_
- using fixture data to simulate REST response
- index.hbs now lists all items returned
- has header
- has footer
- added serializer as documented in https://guides.emberjs.com/v2.3.0/models/customizing-serializers/ to parse through nested objects
- relations ship between issues & projects established
- routing full implemented

##### February 19 2016 #####
- Ember.js framework set
- First model blue prints