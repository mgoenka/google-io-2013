## New features in Android Location

		Goals of the Changes
			Reduce Power
			Improve accuracy
			Simplify the APIs
			Expose cool new features
			Make it available on most Android devices
		New and improved APIs
			Fused Location Provider : Simpler, lower power and more accurate
			Geofencing : Power management
			Activity Recognition : Detect the user's activity using sensor data (Vehicle, On foot, Still, On Bicycle)
			All available today in Google Play Services


##	What’s new in Google Play Services

		Location update Request
		Geofencing
		Activity Recognition
		Play Games 
			Achievements
			Leaderboards
			Cloud save
			Real-time Multiplayer
		Google cloud messaging
		Google Wallet
		Pre-flight Check


## Google Cloud Messaging

		400% growth in 10 months
		200k + QPS
		60+% of most popular apps
		Send to Sync : Surf Server - Surf App – GCM
		APIs : Time To Live and Delay While Idle
		XMPP Endpoint
			Up to 10 connections
			Message streaming with ACKs/NACKs
			Same GCM APIs, no Multicasting
		Sending upstream message : Surf App -> GCM framework -> GCM -> Surf Server
		Error Handling
			No Connection
			Message is too big
		Battery and Network optimization
		GCM Upstream
			Send messages reliably
			Send messages with Low Latency
			Time To Live API
		GCM library meets Play Services
			Old Library Compatible
			New APIs from Froyo+
			Upstream only on Play Services
		User Notifications
		Notification Key
			Max 10 regids per Notification Key
			Notification Key Name is unique
			Available for HTTP and XMPP


## The Freebase APIs : Tapping into Google’s Knowledge Graph (http://goo.gl/PD9Ux)
		The Freebase Knowledge Graph
			Open, crowd-sourced, knowledge graph
			1B+ facts, 40M+ topics, 2k+ types
			Free APIs
			Creative Commons Attribution License
			A Source 
		Autosuggest, Semantic Tagging, Entity Collections, Geosearch Collections, Topical Weblinks
		APIs
			Freebase Search API
			Freebase Topic API
			Google Maps API
		Libraries
			Freebase Search Widget
			Freebase Client Libraries
			jQuery Tag-it


## Dart

		There is no undefined, only null
		No type correction with ==, +


## Chrom DevTools

		Workspaces: Change the code directly from Chrome Dev tools
		Sass: SCSS files can directly be edited from the Dev tools
		This is available on Chrome Canary
		Paul Irish - google.com/+paulirish, @paul_irish, paulirish.com, github.com/paulirish
