hipbot-go (formerly Hipbot-go) - A Hipchat Bot
=====

Hipbot-go is a Hipchat bot written in Go. This was my first Go project.

Hipbot-go is a neat little bot with some awesome functionality. He sits comfortably in your Hipchat room waiting for a command. You can ask Hipbot-go to search for nearby restaurants, find an image given a tag, get the latest New York Times articles from a section, report the weather forecast. These are just examples (see below for full command list).

## Hipbot-go's Commands 
1. **@hipbot nearby sushi**
    * Google Places search for "sushi" near your specified lat & lng
2. **@hipbot nytimes technology**
    * Search recent New York Times articles in the "technology" section
3. **@hipbot image me sunset**
    * Search Flickr for a photo of a "sunset"
4. **@hipbot weather me tomorrow**
    * Get tomorrow's weather
5. **@hipbot trivia me today**
    * Get trivia factoids for today's date (interesting or historical events)
6. **@hipbot trivia me 123**
    * Get trivia on a number "123" (math facts)
7. **@hipbot wolfram me periodic table of elements**
    * Get computational information from Wolfram Alpha on the "periodic table of elements"
8. **@hipbot gopkg math**
    * Get the synopsis and path for the Go[lang] package "math"
9. **@hipbot company logo**
    * Get the logo of your company (url specified by you - see configuration section of the wiki)
10. **@hipbot thesaurus me challenge**
    * Get synonyms for the word "challenge"
11. **@hipbot search me HMAC**
    * Search the web for information on "HMAC" (uses duckduckgo.com for search engine)
12. **@hipbot goodnight**
    * Tell Hipbot-go goodnight! He will respond with a nice farewell
13. **@hipbot foobar baz**
    * Say anything else, and hipbot will respond with "Hello, FirstName LastName"


<br>
	
## Setup & Configuration
### Plain-Ol', Short & Sweet Setup Instructions:
1. Clone the Hipbot-go repo `git clone git@github.com:adams-sarah/hipgo.git`
2. Deploy your Hipbot-go app to a server (<a href='http://heroku.com'>Heroku</a> is an easy one). You'll need to use a custom buildpack on Heroku: `heroku create -b https://github.com/kr/heroku-buildpack-go.git`.
3. Set the necessary environment variables for your Hipbot-go app - list is below.
4. If there's any functionality you don't want to use, be sure to comment it out in `speak.go`.
5. Run hipbot on a worker instance. On Heroku, configuring this is a matter of setting your free Dyno to 'worker' and not 'web'. You can do this at https://dashboard.heroku.com/apps/YOUR-APP-NAME/resources

<br>
	
## Hipbot-go's Environment Varaibles 	
#### External APIs
1. Flickr (`image me`): `FLICKR_API_KEY`
2. New York Times (`nytimes me`): `NYTIMES_API_KEY`
3. Google (`nearby`): `GOOGLE_API_KEY`
4. BigHugeLabs (`thesaurus me`): `BIG_HUGE_LABS_API_KEY`
5. Forecast.io (`weather me`): `FORECAST_IO_API_KEY`
6. Wolfram Alpha (`wolfram me`): `WOLFRAM_API_ID`

#### Hipchat API
1. `BOT_FULLNAME`
2. `BOT_MENTIONNAME`
3. `BOT_PASSWORD`
4. `BOT_USERNAME`
5. `ROOM_API_TOKEN`
6. `ROOM_ID`
7. `ROOM_JID`

#### Other
1. `LAT_LNG_PAIR` (ie. "28.776266,-100.397550")
2. `COMPANY_LOGO_URL`

