sass-grid
=========
> What the hell is this good for? We have plenty of grid frameworks!

I don't want to include tags for different screen-sizes to html-elements ending up to something like:

	<div class="col-lg-3 col-md-4 col-sm-6 col-xs-12">...</div>
	
I think it is better to have something like:

	<div class="some-class">...</div>
	
and (.sass):

	.some-class {
		@include grid-col(3, lg xl);
		@include grid-col(4, md);
		@include grid-col(6, sm);
		@include grid-col(12, xs);
	}

Instead of having a single big css-file, I rather have five smaller ones that load only if a certain media-query was met. So I can easly exclude some elements via *display: none* and omit graphics as well. It is simple to generate stylesheets for different browsers and bother with some browser-specific quirks.