# Bootstrap Progressbar
Simple Bootstrap Progress bar animate on page scroll. We used jquery appear to trigger the animation while you scroll the page.

Click here to view [Demo](https://asifpix.github.io/bootstrap-progressbar/)

## Integration
#### Bootstrap Basic Markup
    <div class="progress">
		<div class="progress-bar" data-percent="60">
			<span class="sr-only">60% Complete</span>
		</div>
	</div>
#### Include jQuery Appear and CountTo Plugin
    <script src="assets/js/jquery.appear.js"></script>
	<script src="assets/js/jquery.countTo.js"></script>
#### Initiating
    (function($){
		"use strict";
		$(document).ready(function(){
			$('.progress-bar').each(function(){
	            var width = $(this).data('percent');
	            $(this).css({'transition': 'width 3s'});
	            $(this).appear(function() {
	                console.log('hello');
	                $(this).css('width', width + '%');
	                $(this).find('.count').countTo({
	                    from: 0,
	                    to: width,
	                    speed: 3000,
	                    refreshInterval: 50,
	                });
	            });
	        });
		});
	})(jQuery);
    
