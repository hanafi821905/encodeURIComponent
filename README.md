# encodeURIComponent

Some images were named with two words with blank space.  Without encodeURIComponent we can display only single word images.
We need to display image based on stored image's file name in JSON API.
Some images were named with two words with blank space. 
Without encodeURIComponent we can display only single word images. 
encodeURIComponent will render all filename such as 
john doe.jpg as john%20doe.jpg

                            var HR_STF_IMG = "defaultBLANKFace.jpg";
							if (jsondata[0].HR_STF_IMG != "")
							{
								HR_STF_IMG = jsondata[0].HR_STF_IMG;
								
							}
							var encodefilename=encodeURIComponent(jsondata[0].HR_STF_IMG); 
							var imgSrc = "http://yourserver.com/img/stf/photos/" + encodefilename;
							$('.profile-background').css('background-image', 'url(' + imgSrc + ')');
							$('.profile-pic').css('background-image', 'url(' + imgSrc + ')');
