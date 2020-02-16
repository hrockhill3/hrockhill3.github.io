---
layout: archive
permalink: /affiliates/
title: "Affiliates"
author_profile: true
header:
  image: "/images/BKbridge.jpg"
---

{% include base_path %}
{% include group-by-array collections=site.posts field="tags" %}

## These are a few things I use to manage my personal finances.
+ I completed my MBA with a portion of my student loan debt at a higher interest rate than I would have liked. Now there are a ton of student loan refinancing options out there and I recommend you do your own research. However, after a careful review of the LIBOR forecast and my expected tax exposure over the remainder of my anticipated pay back period, I decided that a variable rate refinance of a portion of my debt with [Earnest](https://www.earnest.com/invite/harley93) fit my situation the best.

+ If you're still undecided on a commission-free investing platform I would recommend [Robinhood](https://join.robinhood.com/harleyr33). In conjunction with some knowledge of python and their API it's possible to build out a functional commission-free trading model that's a fun way to earn a lunch or two every now and then. If you're interested in learning more about algorithmic trading I learned through [Quantopian](https://www.quantopian.com/tutorials/getting-started). While they no longer support broker integrations it's still a fantastic well knowledge to dip into if you're getting your feet wet or if you want to brush up on a few things.

+ Heralding back to my days as a broke graduate student [Acorns](https://acorns.com/invite/C4D9AQ) Round-Ups feature collects the loose change from in between the couch cushions and the pennies I’d get back from my morning coffee and instead of getting sticky in my car's cup holder they invest it into a portfolio with exposure to thousands of stocks and bonds. Also they cover any trading fees and they automatically reinvest dividends. I treat this as a holding pattern for money that can be invested without much thought or risk. When it makes sense I'll withdraw these funds (usually once a year) and reinvest it in my primary account.


If you or someone you know is looking to learn more about any of the topics my guests or I bring up there are plenty of fantastic titles available on <a target="_blank" href="https://www.amazon.com/hz/audible/gift-membership-detail?ref_=assoc_tag_ph_1524210806852&_encoding=UTF8&camp=1789&creative=9325&linkCode=pf4&tag=hrockhill3g0c-20&linkId=00c1f0b6b9dd29a8138ab3d56aa35031">Audible </a><img src="//ir-na.amazon-adsystem.com/e/ir?t=hrockhill3g0c-20&l=pf4&o=1" width="1" height="1" border="0" alt="" style="border:none !important; margin:0px !important;" />. If you don't have an account already try out a gift membership for a month and listen to [You May Also Like: Taste in an Age of Endless Choice by Tom Vanderbilt](https://www.audible.com/pd/You-May-Also-Like-Audiobook/B01CROB488?pf_rd_p=6a5ce8e4-798e-4a64-8bc5-71dcf66d673f&pf_rd_r=SRBP2D4CY5F3FBAD21KD&ref=a_lib_c4_libItem_B01CROB488) which was a refreshing reprieve from marketing research papers and attempts to help us better understand how all of us perceive, judge, and appreciate the world around us. Or one of my favorites, [Pricing the Future by George Szpiro](https://www.audible.com/pd/Pricing-the-Future-Audiobook/B006FKAUB8?pf_rd_p=6a5ce8e4-798e-4a64-8bc5-71dcf66d673f&pf_rd_r=3YA2KCV5Y0HZ5EF8XX4Q&ref=a_lib_c4_libItem_B006FKAUB8) which tells the story of discovery of the Black-Scholes options pricing formula.

{% for tag in group_names %}
    {assign posts = group_items[forloop.index0] %}
    <h2 id="{{ tag | slugify }}" class="archive_subtitle">{{ tag }}</h2>
    {% for post in posts %}
        {% include archive-single.html %}
    {% endfor %}
{% endfor %}
