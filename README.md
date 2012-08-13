# jQuery Email Link

jQuery plugin for cloaking email links

## How to use

### HTML: Same domain

When the address is on the same domain as the web site:

Eg. the e-mail address is contact@example.com and the web site is www.example.com (or just example.com)

	<span class="e">contact</span>

Result:

	<a href="mailto:contact@example.com" class="e-mail">contact@example.com</a>

### HTML: Different domain

When the address is on a different domain:

Eg. the e-mail address is contact@example.com and the web site is www.foobar.com

	<span class="e">contact / example, com </span>

Result:

	<a href="mailto:contact@example.com" class="e-mail">contact@example.com</a>


### HTML: Custom link text

When the link text should be other that the email address:

	<span class="e" title="Send us an e-mail">contact</span>

Result:

	<a href="mailto:contact@example.com" class="e-mail">Send us an e-mail</a>


### JS, all cases

In all cases init the JS like this:

	(function($) {
		$(document).ready( function() {
			$('.e').emailLink();
		} );
	})(jQuery);

## Options

Possible options:

	var settings = {
		'domainDelimeter' : ' / ',
		'dotDelimeter' : ', ',
		'textSrc'  : 'title' // this is which HTML attribute the custom link text should get it's text from
	};
	$('.e').emailLink( settings );

