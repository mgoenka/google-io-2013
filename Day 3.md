## High Performance Apps with Renderscript

		Some GPU Background
			GPUs have become useful for a lot more than just graphics
				Lots of FLOPs versus CPUs
				Great at many data parallel tasks
			Growth of GPU compute largely spurred by HPC adoption
			Programmable GPUs are arriving on tablets and phones

		Mobile vs Desktop : Very different
			Mobile has a lot of architectural diversity
				Lots of CPUs, even more GPUs
				GPUs in particular are extremely different between vendors
			System resources vary statically and dynamically
				CPU/GPU clock speed? Battery? Processor load? Display resolution? Additional processors?
			Goal : high performance applications without sacrificing performance portability 

		Renderscript
			Platform for high-performance computing across different hardware
				API forcused on entire system, not specific devices
				Runtime handles processor selection dynamically
			Provides a consistent target that runs well across all SoCs
				Performance is the objective, not running on a specific processor
			Influenced by other data-parallel runtimes
		
		Renderscript at 10,000 feet
			Performance-critical kernels are written in a C99-based language
				Kernels distributed with APK as architecture-independent bitcode
				Compiled from bitcode to one or more processor targets at runime.
			Java classes automatically generated for easy integration with existing applications
			Resource management and execution handled by java APIs

		Script Groups
			Allows a group of kernels to be executed as a single call
			Enables the driver to perform various optimizations by knowing the entire workload 
				Scheduling across devices, kernel fusion…
			Significantly faster in some cases today than individual scripts

		Features coming soon
			Compatibility library for Gingerbread
			rsSetElementAt_<type>
			Debug runtime
			Additional script intrinsics
			YUV Allocations
			Improved launch latency

		RS Compatibility Library
			Enables modern RS on devices running Gingerbread or higher
			CPU only, compiles kernels offline for a specific CPU architecture
			Devices running modern Android will use the native RS library
				With GPU acceleration on appropriate devices


## Android : As seen on TV!

		10+ Manufacturers world wide are building Android Devices With Google TV
		Pure Android : No “Special SDK needed”
		Most important feature of any TV App
			<uses-feature android:name=”android.hardware.touchscreen” android:required=”false”>

		Android Focus handling
			Make a concious decision where to place “default” focus to minimize key presses!
			Request default focus for element
				View.requestFocus()
				<requestFocus>
		Explicit control of focus sequence
			android:nextFocusDown
			android:nextFocusLeft
			android:nextFocusRight
			android:nextFocusUp
			android:nextFocusForward

		Know your “Android Features”
			Use the “AAPT” tool to verify all your Manifest tags
			Displays Features, Permissions, etc. “as seen” by Market!
			aapt dump badging MyApplication.apk
				package: name=’com.mydomain.greatapp’ targetSdkVersion:’12’
				uses-feature-not-required : ‘android.hardware.touchscreen’
				uses-feature : ‘android.hardware.wifi’

				uses-permission : ‘android.permission.INTERNET’
				uses-permission : ‘android.permission.ACCESS_WIFI_STATE’

		The New Google TV Platform
			Android API	Honeycomb API Level 13	updated to Jellybean 4.2.2 API Level 17
			Media Delivery	updated to Adaptive Bitrate Streaming of BlueRay HD quality content using Widevine, Play Ready, HLS, Smooth Streaming and Media Source APIs
			Browser	Chrome 11 to Chrome 28 with EME and MSE
			NDK to NDK, ARM ABI

		New Android APIs
			Android API level
				API 17 (Jellybean)
				Default system theme change, Action Bar, etc
				Some Permission defaults changed
					e.g.: No permission to write APN Settings;
						Neither user nor current process has android.permission.WRITE_APN_SETTINGS
			Include Google TV specific API Library
				Use com.google.android.tv.v2.jar library
				Set AndroidManifest.xml
					<uses-library android:name=”com.google.android.tv.v2” />

		GtvMediaPlayer extends android.media.MediaPlayer
			setLowLatency(boolean lowLatencyMode)
				Minimize internal buffers in native player and HW decoder
				Low Latency Streaming Cloud Games
			setMinMediaBitrateForAbr(int kbps)
				Improve ABR Streaming experience
		Close Captioning/QoS
			Extended support for additional Streaming Protocols, HLS, local file

		TV Specific APIs
			Supports many different Streaming Protocols
				HTTP Live Streaming, Smooth Streaming
				Quality of Service analytics
				Open API to implement your own Protocol (Media Source API) 
			Compatible with Industry Standard DRM Solutions Trusted Video Path
				Widevine and PlayReady
				HTML5 Encrypted Media Extensions (EME)
			Integrates with devices in your living room (and in the cloud)
				Media Devices API
			YouTube Hosting
				Full control of the player, embeded, full screen
				Extensive APIs for Playlist control
				Integrated monetization

		Chrome TV Enhancements
			Latest version of Chrome on Android, Version 28 or later
			Full Screen mode
			HTML5 Encrypted Media Extension (EME)
			Media Source Extension for custom Streaming Protocols


## Mobile Web Apps with Dart and Web Components

		Hands-on experience on building declarative, modern mobile web apps with Dart and Web Components. 
		Use of Dart's structured language, comprehensive libraries. 
		Used the Dart toolchain to deploy and test web apps for tablet, phone, and desktop.
		Problem Statement: Build a simple, single page, modern web-app for desktop and mobile.  
		Agenda
			Editor: dartlang.org/editor/
			Followed 8 simple steps to design the app on DART editor
			Refer to attached document: CodeLab 1 Dart 


## UX design for developers

		Hands-on UX workshop for developers interested in UX design to become a part of the design narrative for whatever product they're working on. 
		This one was focused more on developers new to UX design, and want to contribute to the design process.
		Problem Statement: Design a mobile app to order pizza
		Agenda
			Part 1 (Individual activity - Time: 45 mins)  
				Step 1 – Create a persona and use cases
				Step 2 – Designing the app
			Part 2 (Team activity – participants were grouped in a team of 4 – Time: 45 mins)
				Step 1 – Create 3 personas – creating new or composite personas from individual acivity
				Step 2 – Re design your app – support all 3 personas and app should support only 1 use case per persona. 
				Design must fit in less than 9 screens.


## Build a WebRTC Web App

		Used WebRTC to build a simple video and text chat app. 
		WebRTC Technologies: - MediaStream, RTCPeerConnection, RTCDataChannel, signaling, servers, STUN and TURN
		Problem Statement: Build a simple video and text chat application.
		Agenda
			WebRTC enables real-time communication in the browser.
			Followed steps 1 to 7 to build the desired application.
			Refer to attached document: CodeLab 3 WebRTC


## Android Design in action Live

		This was an interactive design lab, showing the process of designing an Android app – from feature-planning to sketching and drawing screen wireframes.
		At the end of the session, participants were asked to present their design to the audience. 
		Problem statement: Design an interactive mobile banking application for teenagers.
		Agenda
			Intro (15 mins)
			Planning information and architecture (20 mins)
			Create a screen map (20 mins)
			Sketch and wireframe your UI (45 mins)
			Presentation and judging (30 mins)
