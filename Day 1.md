Keynote
==============

## Android

		Location APIs Ð geo-fencing, user activity awareness
		Mobile games - multi player games
		Android Studio -  release of development tool,  multi configuration for different layouts, easier internationalization
		Google play developer console - optimization tips, app translation service (choose translation vendor, about a week the app can be downloaded from the developer console), referral tracking  from Google analytics to integrate in the developer console (this feature is going out this summer), revenue tab to display revenue, three tabs in developer console - production, beta testing, alpha testing and staged rollouts
		Design of new Google play store - designed for tablets,  similar design of Google play store on the website
		Music streaming service -  Google play music ÔAll AccessÕ music subscription service, $9.99/month, launching in US today
		Galaxy S4 - stock android OS available in Google play store in June


## Chrome

		Chromebook, demoing WebGL based games
		Design philosophy - speed, simplicity, security
		asm.js for speed improvement
		WebP image is 30% lesser in size than jpeg, good for mobile, and web
		H.264 vs VP9 - VP9 60% lesser in size, youtube will support VP9 later this year
		Data compression on chrome for mobile
		Google wallet - consolidating form fields in payment form for ease of use
		Demoing racing games - using websocket, multiple devices with different sizes are connected to create one screen
		Free Chromebook Pixel for all the developers


## Education

		Google play for education launching this fall by category which will focus on tablet apps for children


## Google+ (Stream, Hangout, Pictures)  

		Multi column design, automatic hashtags for the posts
		Rebranding Google Talk to Hangout, tightly integrating Google+ features, free video call
		Integrating camera with cloud - 8MP size upload in Google+
		Picture - highlights, auto enhancement of the pictures which will be rolled out today (Ôenhance buttonÕ)
		Auto awesome feature


## Search

		Knowledge graph - search to move beyond keyword, launching support for new languages
		Conversation search on desktop
		Google now cards -  reminders, public transit, multimedia contents (games, TV shows, books, music albums)


## Google maps

		199 countries launched on Google maps
		50 countries in street view
		Integrating maps with eats, shops, sleeps.
		Indoor map



Sessions
==============

## Google Maps: Into the future

		Google online course on map in June: ÒMapping with GoogleÓ online course
		The NEW Google Maps API
			The Obvious question? Are you going to announce a new maps api
			The new Google Maps is a Preview
		Maps API Comparison
			JavaScript Maps API 2006 (Red Pin, Info Window, large shadow)
			JavaScript Maps API 2013 (Square edges of the info window)
			Loads on new features but still the same product
		New refresh feature
			google.maps.visualRefresh = true;
			Major Changes -> New default marker, new info window, New Look controls
			Seamless Transition
		Javascript maps api V3
			google.maps.visualrefresh=true;
			for refreshing ui design, render same as map rendered in mobile, new marker, new info window look
		Static Maps API V2
			&Visual_referesh = true;
			1 line of code changes the whole thing
			For a preview of all the new features visit http://www.morethanamap.com/
			Available now on experimental and release branches
			Default on Experimental: Aug 15
			Default on Release: Nov 15
		The next Million maps
			Taking Maps to the next platforms
			Same Google Data on Three Platforms (Chrome, Android, IOS)
			Mobile is not the future, it is the present
			Mobile Data is 13% of Global Internet Traffic
			Larger in some places, In India: 60%
		(On)-Location is the present.
			Updates on both Android and IOS
			Android Maps Android API V2
			Power of consumer Google Maps for Android renderer for developers
			Automatically updated to end users devices Via Google Play services
		Google Maps SDK for iOS
			Google Maps for iPhone Renderer
			Easy integration with existing apps
			URL scheme to launch Maps app
		Indoor Maps: The Next Frontier
			Why?
				We spend 90% of time indoor
				Tokyo - 100% indoor
				Find something indoor (ATM, restroom, coffee, etc)
			Why is it difficult?
				POIs can be very different as per types of buildings
				At least 6 meter of accuracy is required to be useful for indoor navigation
			Indoor maps coverage + high quality indoor location + self-service tools + growing developer APIs + tipping points?
			What makes indoor hard?
				Maps information (name of roads, etc) - where from? - how to verify?
				Location information
					GPS doesn't work
					What floor am I on? (barometer is not usable. air pressure is not stable.)
			Where are we?
				SFO (example) - check-in, restaurants, security, gates, etc. Search - find all venues on every floor
				Indoor map launched in 13 countries
				station, indoor path to another building, museum
			How it works?
				Create a map - add your floor plan, find your building, upload your floor plan, align the floor plan to the building -> Google'll trace your maps
				Provide high quality location - WiFi+GPS+Sensors

 
## Importing large datasets into Google Cloud Storage

		Google cloud storage - features for http connection optimization
		Small to medium imports
		gsutil (network latency limitation) https://developers.google.com/storage/docs/gsutil
		Cloud storage
		Large imports - gsutil -m cp (-m for multi processing, multi threading)
		Limitation - network bandwith/disk io/coordination, complexity
		Compose - limit to 32 pieces, but it takes 32 pieces and combine into one
		Large data migration case Ð post processing: notification and JSON batch requests, JSON API batch requests - for multiple updates
		Offline disk import support - limited preview, for us only, $80 per disk
		Feature releases - cloud console, composite objects, notification, JSON APIs, offline disk import


## Androids Do Daydream - System UI team

		Android 4.2 - day dream
		Dock mode - had to do screensaver
		Dock app - customized UX, easy to access, ambient info, but confusion
		Writing dock app is tricky - nitty gritty things to consider
		Dream in 4.2 -  easy to write, full drawing API support, full touch/interaction
		Dream will start when - while docked (dock app), while charging (screen saver), for both, \unless something is holding a wake lock
		Dream - access to full UI kit


## 7 Techmakers and a microphone

		Need insight - what would make it product break, youtube example
		Ad is information
		Current focus is location based services
		Product management is to - paint the vision, need to do something by create a small milestone, listen to your user, use your product as much as you can
		Google Glass hardware design over view - main design criteria: power consumption and weight


## Google Wallet: Selling physical goods on Android with Google Wallet Instant Buy

		Typical mobile checkout requires 24+ steps
			Shopping cart, Confirm Order, Fill out forms, Order Complete, shipping address etc
		As per a recent survey 97% of users abandon a mobile purchase in mid-flow
		Introducing Google Wallet Instant Buy
			Faster checkout for physical goods
			Skip registration and sign in
			Secure
			Lightweight integration
			No additional fees
		Checkout -> buy with Google -> Chooser screen (card, shipping address) - Skip after first time -> Order Confirmation
		Priceline App Example:
			Priceline -> VP of Mobile 
			Google Wallet support fully integrated into the priceline android application
		Faster Checkout - Backend Process:
			Four Steps:
				Get a masked Wallet
				Show instant buy UI
				Update your UI
				Get a full wallet
		Integrating Instant Buy
			Wallet Branded button
			Establish Connection
		Instant Buy Architecture
			Part of Google Play services
			All android 2.2+ devices with Play store
			Thin client Library compiled in your app
		Getting a Masked Wallet
			Build a request
			Full Billing address?
			Shipping address?
			Phone number?
		Show Instant Buy UI
			Callbacks receive a connectionResult (Success or failure)
			Success = data, no UI to show
			Failure = Need to show UI
			StartActivityForResult
		Using the Masked Wallet
			Confirm the order
		No registration or login
			Apps integrated with Google + and Google Wallet (Social sharing)
		Secure
			Easier and more secure
			Fraud protection - Google Wallet Purchase protection
		Why Instant Buy
			Faster checkout for Physical goods
			Skip registration and sign in 
			More secure
			Lightweight integration
			No fees
		Early access: http://getinstantbuy.withgoogle.com/
		Few feature: Send Money without leaving your Gmail inbox
			Without leaving your Gmail Inbox
			Easy and convenient 
			Free
			Secure


## Google Drive on Android - The mobile storage solution

		Example: Baby monitors - loads of apps
		Application Demo: BABY ESP - Perfect for the use case.
			No seamless cross device experience
 		Use drive to solve this problem
			Integrate your app with Google Drive
			Access EDIT and SAVE your apps in drive
 		Where is my data? Where are my files?
			Store my data where I need it 
			Somewhere I can share it with people and applications
			All Gmail user have 5GB free Drive storage
 		How do we do it?
		Data is stored in 2 diff locations
			App Data
			Regular Drive files
		Design your Data as normal
			User Input -> SQL database
			Export a Google Spreadsheet
			This data is portable across DEVICES, APPLICATIONS, and USERS
 		App Data folder permissions:
			View -> No
			Edit -> No
			See Quota -> Yes
			Delete -> Yes
		Multiple O Auth2.0 clients per project
			Authorization Scope
				Refer: www.googleapis.com/auth/drive.appdata
				Fork the code on Github
				Put the data where I want it 
				Treat me as a user, not as a device
				Create seamless cross platform applications with Google drive
