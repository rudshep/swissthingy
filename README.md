Tinkering with electronics is fun and entertaining when it works but quickly gets frustrating if you do not have the right tools to test, measure, diagnose, debug and fix your creations.

Taking inspriration from the venerable Swiss Army Knife - and The Guy with the Swiss Accent, SwissThingy aims to put a bunch of useful little tools and tests into something that can easily fit on your pocket and be thrown into the toolbox ready for the next project.

This is a project meant to solve my own personal tinkering needs but if you find it useful, please contribute ideas, hardware and code to make it better.

So, let's get started with the basics... things every "serious" electronics toolbox needs...

- A Multimeter that can measure Volts, Amps, Resistance, Continuity, Frequency and Capacitance.
- Bonus if it has a graphical display of the values over time. Then it is basically an Oscilloscope isn't it!
- A Signal Generator to generate, well, arbitrary signals - like sine waves, square waves, triangle waves and sound of music waves.
- A Logic Analyzer to see all those toggling bits on a digital bus fly past.

That's pretty much already a serious test and measurement instrument and the domain of professional manufacturers like Keysight, Rigol, Tektronix and other big names. Personally I have a Rigol 'scope and logic analyzer on my bench but often find myself needing to do a quick test on a thing installed somewhere in my house and don't want to schlep the 'scope over there. Perfect use case for SwissThingy.

However, it needs to be clear that SwissThingy is an amateur DIY device and nowhere near the features and specs of a professional piece of equipment. Dave will cringe when he sees this no doubt! My aim is to have something simple that ElectroBoom can safely use without killing himself and Big Clive will give a stamp of "not entirely crap" approval.

Moving swiftly along...

At this very moment I am busy hacking my Grid Tied Inverter system to pull data off and get it into Home Assistant. The problem is I need to sniff the communication protocol it uses off the serial port and inject commands of my own. To do this, I need a Serial Bridge, Protocol Analyzer and a simple Serial Terminal while I'm at it. So these will be the three modules I'll be working on first for the SwissThingy version 1.0.

Before I can do that, I will need a Core to handle the user interface, menu system, hardware interfacing, over the air update and logging. The architecture is starting to take shape...

Measure
	Multimeter
		Volts, Amps, Ohms, Hertz
	Oscilloscope
		Volts/Div
		Time/Div
	Logic Analyzer
		Ch1, Ch2, Ch3, Ch4
	Counter
		Count
		Reset
	Sensor
		Wifi
			Scan
		BLE
			Scan
		Hall
			Interval [s]
		Switch
		Duty Cycle
		UART
      Baud
      Bits
      Start Bits
      Stop Bits
    1-Wire
		I2C
		SPI
Generate
	Sine
		Frequency [Hz]
		Amplitude [%]
	Square
		Frequency [Hz]
	Triangle
		Frequency [Hz]
		Amplitude [%]
	Pulse
		On Time [ms]
		Off Time [ms]
		Repeat [count]
	PCM
		File
	Servo
		Position [%]
		
	UART
		Serial
		Midi
		Modbus
	MQTT
	IP
		HTTP
		UDP
	IR
	LED
	I2C
	SPI

