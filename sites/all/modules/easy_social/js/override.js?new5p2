jQuery(document).ready(function(){
	//global vars
	var source_page = window.location.href;
	var tw_meta = {}; 
	var fb_meta = {};
	
	//gather metadata
	jQuery('meta').each(function(){
		var prop = jQuery(this).attr('property');
		//facebook
		if(prop!== undefined && prop.match('og:') ){
			fb_meta[prop] = jQuery(this).attr('content');
		}
		//twitter
		if(prop!== undefined && prop.match('twitter:') ){
			tw_meta[prop] = jQuery(this).attr('content');
		}
	})
	
	//twitter
	if(tw_meta['twitter:creator']){
			tw_meta['twitter:account'] = tw_meta['twitter:creator'];	
		}
	var twitter_wrap = jQuery('.easy_social-widget-twitter');
	var twitter_btn = '<a href="https://twitter.com/share" class="twitter-share-button" data-url="'+ tw_meta['twitter:url'] +'" data-via="'+ tw_meta['twitter:account'] +'" data-lang="en" data-related="anywhereTheJavascriptAPI">Tweet</a>'
	twitter_wrap.children().remove();
	jQuery(twitter_wrap).append(twitter_btn);

	//console.log(fb_meta);
	//console.log(tw_meta);
})
