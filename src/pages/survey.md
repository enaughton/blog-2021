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
	window.Kno = { 
			kno_id: 'B0F38NN-60F4SAJ-QY8ZKT9-16ZHSAD',
			customer: { 
					platform: 'CUSTOM',
					shop: 'emmettnaughton.com', 
					email: 'enaughton5@example.com', // required if no phone.
					phone: '1234567894', // required if no email. Must use this format.
					id: 'id-from-some-platform', // optional. Must be a string.
					lifetime_spent: 452.12,
					lifetime_orders: 2
			},
			order: {
					id: '1234567892', 
					total_price: 1000,
					currency: '',
			},
			survey : {
				selector: 'div#example_element_for_insert' 
	 		} 
	};
	

	
</script>

<script src="https://www.knocdn.com/v1/embed.js?id=f33d093a-e0ba-4854-a121-a9963f0f9fad"></script>
<div id="example_element_for_insert"></div>
</html>