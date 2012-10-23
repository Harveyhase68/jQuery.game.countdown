GameCountDown
=============

jQuery.game.countdown - a jQuery Plugin

The advantage of this countdown plugin is, many countdowns on a page don't slow down the website, because only one timer exist.

jQuery.game.countdown accecpts only remaining seconds. If you need a specific date to count to, this is the wrong plugin for you.

jQuery.game.countdown, displays a text in a div tag, like '9d 15h 12m 34s' and countdown.

Any issues and suggestions welcome, write to me at: guthub@predl.cc

You need a copy from jQuery (http://www.jquery.com)

Download Updates from my script anytime: https://github.com/Harveyhase68/jQuery.game.countdown or http://www.predl.cc

	<script type="text/javascript" src="js/jquery-1.8.2.min.js"></script>
	<script type="text/javascript" src="js/gamecountdown.min.js"></script>

First of all you need a new countdown class:

	GameCountDown = new $.GameCountDown();

Second Add any timer you wish (the timer will start immediately):

	GameCountDown.Add({control: '#counter1', seconds: 5});

Of course a div with the appropriate tag needs to exist:

	<div id="counter1"></div>

Options for GameCountDown:

	unit: (default 1000) milliseconds, intervall of the timer(s)
	readymessage: (default 'fertig!'), displays a ready text, when the counter goes zero
	displayreverse: (default false), reverse order of counting (counting up instead of down)
	displaymax: (default false), displays a '/' and the maximum of the counter
	formatday: (default 'd '), additional text for days
	formathour: (default 'h '), additional text for hours
	formatminute: (default 'm '), additional text for minutes
	formatsecond: (default 's'), additional text for seconds
	callback: a javascript callback function script global

Options for function Add:

You cannot add two time the same control, use Set if you wish to update a counter anytime.

	control: a jQuery control like '#counter1' or '.counter' (will add all controls with class 'counter')
	seconds: (default 60), amount of seconds to countdown
	callback: a javascript callback function only for this counter

Options for function Remove:

The countdown will stop for each control

	Remove('#counter1');

only a parameter with a jQuery control ('#counter1' or '.counter' will remove all controls with class 'counter')

Options for function Set:

The counter will start new on 'seconds' for each control

	control: a jQuery control like '#counter1' or '.counter' (will update all controls with class 'counter')
	seconds: (default 60), amount of seconds to countdown
	callback: a javascript callback function only for this counter

