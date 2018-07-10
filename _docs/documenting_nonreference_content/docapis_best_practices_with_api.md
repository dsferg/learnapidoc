---
title: API best practices
permalink: docapis_best_practices_with_api.html
keywords:
course: "Documenting REST APIs"
weight: 5.9
sidebar: docapis
section: docnonref
path1: /docnonref.html
---

API best practices can refer to any general advice your product team wants to communicate to developers about working with the API. There's no set number of topics or content that is typically covered in API best practices. Instead, the best practices can be a catch-all title for content that doesn't fit anywhere else.

* TOC
{:toc}

## What topics to include in best practices

Although many of the topics in API documentation are standard, there will usually be a laundry list of things to know about working with the API. You can only probably get this information by asking the developers.

The list of topics might include topics such as the following: pagination, time ranges, fault tolerance, cache values, connectivity, timeouts, downtime, SSL, versions, testing and validation, exports, languages, number handling, expanding resources, notifications, CORS, localization, and more.

{% include course_image.html size="medium" border="true" filename="nonref_bestpractices" ext_print="png" ext_web="svg" alt="Best practices" caption="Best practices cover a range of topics usually unique to your API" %}

{% include random_ad2.html %}

## Sample API best practices

The following are API best practices from several API documentation sites.

### Mailchimp

{% include course_image.html url="http://developer.mailchimp.com/documentation/mailchimp/guides/mailchimp-api-best-practices/" filename="bestpractices_mailchimp" ext_print="png" ext_web="png" alt="Mailchimp API best practices" caption="Mailchimp best practices" %}

Mailchimp's API best practices include tips about fault tolerance, using specific requests, authentication, cache values, connectivity, and registration. With fault tolerance, Mailchimp reminds developers that outages sometimes happen, so they should plan to handle scenarios accordingly if the API doesn't respond. With specific requests, Mailchimp warns users about the time it can take if the request is too general and hence returns too much information.

{% include random_ad.html %}

### Coinbase

{% include course_image.html url="https://developers.coinbase.com/api/v2#pagination" filename="bestpractices_coinbase" ext_print="png" ext_web="png" alt="Coinbase best practices" caption="Mailchimp best practices" %}

Coinbase doesn't specifically refer to these topics as best practices; instead the navigation just shows a laundry list of topics. Pagination is one of these topics worth expanding on here. What is pagination in relation to an API? Suppose your API endpoint returns all items in a user account. There could be thousands of items, and if all items were returned in the same response, it might take a long time for the API to gather and return the large amount of data. As a result, just like with searches on Google, the response returns a limited set, such as the first 10 items, and then includes a URL that you can use to go to the next set of responses. Pagination refers to advancing to the next page of responses.

Earlier, when defining the characteristics of REST, I mentioned [HATEOS](docapis_what_is_a_rest_api.html#stateless_and_cacheable), or "Hypermedia as the Engine of Application State." Links in responses that return more results is one example.

Programmatically handling the URL to get more responses can be kind of tricky. If you want to get all items returned and then filter and sort the items, looking for specific values to pull out, how would you do this using the URL returned in the response? Your team might have some advice for developers handling these scenarios. Most likely, the endpoint would offer filters as parameters to apply to the endpoint, so that the initial response would contain the item set you wanted. This kind of advice might be appropriate in API best practices.