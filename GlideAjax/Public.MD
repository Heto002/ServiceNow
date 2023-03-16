In the case where you want other users to use your Glide Ajax, you will need to add:  
  
	isPublic: function () {  
		return true;  
	},  
...at the top of your exisitng script include (should be the first function)
