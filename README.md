# Simple-Hide-Show-Accordion
Simple Hide/Show Accordion

a simple light responsive slide toggle accordion.

Demo page coming soon.

***
###Styling

Styling by changing the following classes.

.accordion-tab {
	font:bold 12px/35px "Days One",sans-serif;
}
.accordion-tab {
	background: #f3f3f3;
}

/* CHANGE OPEN & CLOSE TOGGLE IMAGE to FONTAWESOME */
div.accordion-tab:after {
	background:#3276b1 url('../images/toggle_open.png') center right no-repeat;
}
.accordion-tab.active:after {
	background: #3276b1 url('../images/toggle_closed.png') center right no-repeat;
}

Change the above CSS to:

div.accordion-tab:after {
	content: "\f0fe";
}

.accordion-tab.active:after {
	content: "\f146";
}


***
##The Markup

	<div id="accordion-container">

		<div class="accordion-tab active">Content #1</div>
			<div class="accordion-content">

		 Integer euismod lacus luctus magna. Quisque cursus, metus vitae pharetra auctor, sem massa mattis sem, at interdum magna augue eget diam. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Morbi lacinia molestie dui. Praesent blandit dolor. Sed non quam. In vel mi sit amet augue congue elementum. Morbi in ipsum sit amet pede facilisis laoreet. Donec lacus nunc, viverra nec.

			</div> 

		<div class="accordion-tab">Content #2</div>
			<div class="accordion-content">
				
			<p><i class="fa fa-quote-left fa-2x pull-left fa-border"></i>
			...Lorem ipsum dolor sit amet, consectetur adipiscing elit...
			 Integer nec odio. Praesent libero. Sed cursus ante dapibus diam.
			 Sed nisi. Nulla quis sem at nibh elementum imperdiet. Duis sagittis ipsum. Praesent mauris. </p>
			</div> 

		<div class="accordion-tab">Content #3</div>
			<div class="accordion-content">	

		Fusce ac turpis quis ligula lacinia aliquet. Mauris ipsum. Nulla metus metus, ullamcorper vel, tincidunt sed, euismod in, nibh. Quisque volutpat condimentum velit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.
			</div> 
		<div class="accordion-tab">Content #4</div>
			<div class="accordion-content">

		Sed dignissim lacinia nunc. Curabitur tortor. Pellentesque nibh. Aenean quam. In scelerisque sem at dolor. Maecenas mattis. Sed convallis tristique sem. Proin ut ligula vel nunc egestas porttitor. Morbi lectus risus, iaculis vel, suscipit quis, luctus non, massa.

			</div>

	</div>
	
***
##The JS

	Make sure jquery is loaded.

		(function($){
			$(document).ready(function() {
				$(".accordion-content").hide();
				    $(".accordion-content:first").show(); // Remove this line to have first item hidden
				$(".accordion-tab").click(function(){
				if ($(this).is(".active"))
				{
					$(this).removeClass("active");
					$(this).next(".accordion-content").slideUp(400);
					}
					else
					{
					$(".accordion-content").slideUp(400);
					$(".accordion-tab").removeClass("active");
					$(this).addClass("active");
					$(this).next(".accordion-content").slideDown(400);
				}
				});
			});
		})(jQuery);

***
###Callback Options


	$(".accordion-content:first").show(); 			 // Show the first item on accordion (Default)
	
	- Remove the above line to keep all items hidden.
		 	 // callback on accordion load

***
###Changelog

**v1** - 6/02/2015

 - first release
