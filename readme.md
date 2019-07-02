# Web Timestamp Standard

## Properties
Required fields.

### Post
* title
* content
* date (string, ISO 8601)

## Attributes
Optional fields, to be defined in markup.
* previousVersion (string, SHA265)

## Hashing
A hash will be created of an JSON object, containing the required properties and optional attributes in a required order.
```
{
  "title": "Hello World",
  "content": "Hello World",
  "date": "2019-07-01T08:57:08+00:00",
  "previousVersion": ""
}
```

## Markup

Example `microdata` markup for the BlogPosting schema. The markup should include the schema type, schema version, the properties for the type, optional attributes with both the key as value. 
```
<div itemid="http://techcrunch.com/2015/03/08/apple-watch-event-live-blog" itemscope itemtype="http://schema.org/LiveBlogPosting">
  <div itemprop="about" itemscope itemtype="http://schema.org/Event">
    <span itemprop="startDate" content="2015-03-09T13:00:00-07:00">March 9, 2015 1:17 PM</span>
    <meta itemprop="name" content="Apple Spring Forward Event" />
  </div>
  <meta itemprop="coverageStartTime" content="2015-03-09T11:30:00-07:00" />
  <meta itemprop="coverageEndTime" content="2015-03-09T16:00:00-07:00" />
  <h1 itemprop="headline">Apple Spring Forward Event Live Blog</h1>
  <p itemprop="description">Welcome to live coverage of the Apple Spring Forward …</p>
  <div itemprop="liveBlogUpdate" itemscope itemtype="http://schema.org/BlogPosting">
    <h2 itemprop="headline">See the new flagship Apple Retail Store in West Lake, China.</h2>
    <p><span itemprop="datePublished" content="2015-03-09T13:17:00-07:00">March 9, 2015 1:17 PM</span></p>
    <div itemprop="video" itemscope itemtype="http://schema.org/VideoObject">
      <img itemprop="thumbnail" src="http://images.apple.com/live/2015-mar-event/images/908d2e_large_2x.jpg" />
    </div>
  </div>
  <div itemprop="liveBlogUpdate" itemscope itemtype="http://schema.org/BlogPosting">
    <h2 itemprop="headline">iPhone is growing at nearly twice the rate of the rest of the smartphone market.</h2>
    <p><span itemprop="datePublished" content="2015-03-09T13:13:00-07:00">March 9, 2015 1:13 PM</span></p>
    <img itemprop="image" src="http://images.apple.com/live/2015-mar-event/images/573cb_xlarge_2x.jpg"/>
  </div>
  <div itemprop="liveBlogUpdate" itemscope itemtype="http://schema.org/BlogPosting">
    <h2 itemprop="headline">Coming this April, HBO NOW will be available exclusively in the U.S. on Apple TV and the App Store.</h2>
    <p><span itemprop="datePublished" content="2015-03-09T13:08:00-07:00">March 9, 2015 1:08PM</span></p>
    <p itemprop="articleBody">It's $14.99 a month.<br> And for a limited time, …</p>
  </div>
</div>
```
