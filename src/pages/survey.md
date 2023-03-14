---
layout: layouts/page.njk
title: Survey
permalink: /survey/index.html
---
<html>
<div style="padding:50px;text-align:center">
	<h1>There should be a survey here.</h1>
	
</div>
<script defer>

	// below is the data you'll need to add Kno to your custom store.

	// Simple Example with required fields
	window.Kno = { 
			kno_id: 'B0F38NN-60F4SAJ-QY8ZKT9-16ZHSAD', // this is the API key found in the "custom" integration in Settings -> Integration
			customer: { 
					platform: 'CUSTOM', // required. Accepts CUSTOM, WOOCOMMERCE, etc, or anything you want to add.
					shop: 'emmettnaughton.com', 
					email: 'enaughton5@example.com', // required if no phone.
					phone: '1234567894', // required if no email. Must use this format.
					id: 'id-from-some-platform', // optional. Must be a string.
					lifetime_spent: 452.12,
					lifetime_orders: 2
			},
			order: { 
					platform: 'CUSTOM', // highly recommended if you collect data from multiple order systems. Will  Accepts CUSTOM, WOOCOMMERCE, etc, or anything you want to add. Defaults to customer.platform when not found.
					id: '1234567892', // required. Must be a string.
					total_price: 1000,
					currency: '',
			},
			survey : { 
					//id: '824b9cec-1bf6-457b-9a58-6a3888fcdeaf', // optional. the Kno id of your survey. Found in the url when editing a survey. Doesn't need to be set.
					selector: 'div#example_element_for_insert' // required. The element you want to attach the survey to. Survey will be inserted after this element.
	 		} 
	};
	

	
</script>
<!-- insert your script 
	found in the Settings -> Survey Settings -> Miscellaneous 
-->
<script src="https://www.knocdn.com/v1/embed.js?id=f33d093a-e0ba-4854-a121-a9963f0f9fad"></script>
<div id="example_element_for_insert"></div>
</html>