# Shopify-Tag-Cloud
Creates a tag cloud for Shopify blogs.

Works by counting up the tags and turning the count output into a numerical operator. CSS rules determine that tags with larger counts get larger font sizes. <br />
<img src="https://github.com/namurray/Shopify-Tag-Cloud/blob/master/screenshot-loveisproject.myshopify.com%202016-11-21%2014-36-19.png?raw=true" />

<h2>Instructions</h2>
Place tag-cloud.liquid snippet where you want your cloud to appear in blog.liquid, OUTSIDE of pagination rules.

Line 2: Replace BLOG-HANDLE with your blog's handle, eg:  {% for tag in blogs['my-blog'].all_tags %}

<h2>LIMITATIONS</h2>
Shopify only pulls meta data (eg tags) for the first 50 blog posts (see https://ecommerce.shopify.com/c/ecommerce-design/t/blog-tag-count-is-wrong-134716), so your tag cloud tag count will never reflect your full blog if you have more than 50 posts. For this reason, I did not include the actual count next to the tag handles. If you have fewer than 50 blog posts at any given time, you can add ({{ count }}) next to {{ tag }} in line 15 to display the count [eg: Home (12) Garden (10)]. I also suggest adding {{ count }} while implementing this to test it.
