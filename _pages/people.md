---
layout: single
permalink: /people/
title: "People"
header:
  overlay_color: "#5e616c"
  overlay_image: /assets/images/publications.png
---
The collective is loosely organized, and takes valuable input and contributions from a wide group of people. The following people, in no particular order, are heavily committed into our work:

<hr>

{% for author in site.data.authors %}
<div itemscope itemtype="http://schema.org/Person" class = "people-page">

  <div class = "author__bio-wrapper" id="{{author[1].github}}" >
    {% if author[1].avatar %}
      <div class="author__avatar">
        {% if author[1].avatar contains "://" %}
          <img src="{{ author[1].avatar }}" alt="{{ author[1].name }}" itemprop="image">
        {% else %}
          <img src="{{ author[1].avatar | absolute_url }}" class="author__avatar" alt="{{ author[1].name }}" itemprop="image">
        {% endif %}
      </div>
    {% endif %}

    <div class="author__content">
      <h2 class="author__name" itemprop="name">{{ author[1].name }}</h2>
      {% if author[1].bio %}
        <p class="author__bio" itemprop="description">
          {{ author[1].bio }}
        </p>
      {% endif %}
    </div>
  </div>

  <div class="author__urls-wrapper">
    <button class="btn btn--inverse">{{ site.data.ui-text[site.locale].follow_label | remove: ":" | default: "Follow" }}</button>
    <ul class="author__urls social-icons">
      {% if author[1].location %}
        <li itemprop="homeLocation" itemscope itemtype="http://schema.org/Place">
          <i class="fa fa-fw fa-map-marker" aria-hidden="true"></i> 
          <span itemprop="name"> {{ author[1].location }} </span>
        </li>
      {% endif %}
      
      {% if author[1].uri %}
        <li>
          <a href="{{ author[1].uri }}" itemprop="url">
            <i class="fa fa-fw fa-chain" aria-hidden="true"></i> 
              {{ site.data.ui-text[site.locale].website_label | default: "Website" }}
          </a>
        </li>
      {% endif %}
      
      {% if author[1].email %}
        <li>
          <a href="mailto:{{ author[1].email }}">
            <i class="fa fa-fw fa-envelope-square" aria-hidden="true"></i>
            <meta itemprop="email" content="{{ author[1].email }}" />
            {{ site.data.ui-text[site.locale].email_label | default: "Email" }}
          </a>
        </li>
      {% endif %}
      
      {% if author[1].keybase %}
        <li><a href="https://keybase.io/{{ author[1].keybase }} " itemprop="sameAs">
          <i class="fa fa-fw fa-key" aria-hidden="true"></i> 
          Keybase
        </a></li>
      {% endif %}
      {% if author[1].twitter %}
        <li><a href="https://twitter.com/{{ author[1].twitter }}" itemprop="sameAs">
          <i class="fa fa-fw fa-twitter-square" aria-hidden="true"></i> 
          Twitter
        </a></li>
      {% endif %}
      {% if author[1].facebook %}
        <li><a href="https://www.facebook.com/{{ author[1].facebook }}" itemprop="sameAs">
          <i class="fa fa-fw fa-facebook-square" aria-hidden="true"></i> 
          Facebook
        </a></li>
      {% endif %}
      {% if author[1].google_plus %}
        <li><a href="https://plus.google.com/+{{ author[1].google_plus }}" itemprop="sameAs">
          <i class="fa fa-fw fa-google-plus-square" aria-hidden="true"></i> 
          Google+
        </a></li>
      {% endif %}
      {% if author[1].linkedin %}
        <li><a href="https://www.linkedin.com/in/{{ author[1].linkedin }}" itemprop="sameAs">
          <i class="fa fa-fw fa-linkedin-square" aria-hidden="true"></i> 
          LinkedIn
        </a></li>
      {% endif %}
      {% if author[1].xing %}
        <li><a href="https://www.xing.com/profile/{{ author[1].xing }}" itemprop="sameAs">
          <i class="fa fa-fw fa-xing-square" aria-hidden="true"></i> 
          XING
        </a></li>
      {% endif %}
      {% if author[1].instagram %}
        <li><a href="https://instagram.com/{{ author[1].instagram }}" itemprop="sameAs">
          <i class="fa fa-fw fa-instagram" aria-hidden="true"></i> 
          Instagram
        </a></li>
      {% endif %}
      {% if author[1].tumblr %}
        <li><a href="https://{{ author[1].tumblr }}.tumblr.com" itemprop="sameAs">
          <i class="fa fa-fw fa-tumblr-square" aria-hidden="true"></i> 
          Tumblr
        </a></li>
      {% endif %}
      {% if author[1].bitbucket %}
        <li><a href="https://bitbucket.org/{{ author[1].bitbucket }}" itemprop="sameAs">
          <i class="fa fa-fw fa-bitbucket" aria-hidden="true"></i> 
          Bitbucket
        </a></li>
      {% endif %}
      {% if author[1].github %}
        <li><a href="https://github.com/{{ author[1].github }}" itemprop="sameAs">
          <i class="fa fa-fw fa-github" aria-hidden="true"></i> 
          Github
        </a></li>
      {% endif %}
      {% if author[1].stackoverflow %}
        <li><a href="https://www.stackoverflow.com/users/{{ author[1].stackoverflow }}" itemprop="sameAs">
          <i class="fa fa-fw fa-stack-overflow" aria-hidden="true"></i> 
          Stackoverflow
        </a></li>
      {% endif %}
      {% if author[1].lastfm %}
        <li><a href="https://last.fm/user/{{ author[1].lastfm }}" itemprop="sameAs">
          <i class="fa fa-fw fa-lastfm-square" aria-hidden="true"></i> 
          Last.fm
        </a></li>
      {% endif %}
      {% if author[1].dribbble %}
        <li><a href="https://dribbble.com/{{ author[1].dribbble }}" itemprop="sameAs">
          <i class="fa fa-fw fa-dribbble" aria-hidden="true"></i> 
          Dribbble
        </a></li>
      {% endif %}
      {% if author[1].pinterest %}
        <li><a href="https://www.pinterest.com/{{ author[1].pinterest }}" itemprop="sameAs">
          <i class="fa fa-fw fa-pinterest" aria-hidden="true"></i> 
          Pinterest
        </a></li>
      {% endif %}
      {% if author[1].foursquare %}
        <li><a href="https://foursquare.com/{{ author[1].foursquare }}" itemprop="sameAs">
          <i class="fa fa-fw fa-foursquare" aria-hidden="true"></i> 
          Foursquare
        </a></li>
      {% endif %}
      {% if author[1].steam %}
        <li><a href="https://steamcommunity.com/id/{{ author[1].steam }}" itemprop="sameAs">
          <i class="fa fa-fw fa-steam-square" aria-hidden="true"></i> 
          Steam
        </a></li>
      {% endif %}
      {% if author[1].youtube %}
        <li><a href="https://www.youtube.com/user/{{ author[1].youtube }}" itemprop="sameAs">
          <i class="fa fa-fw fa-youtube-square" aria-hidden="true"></i> 
          YouTube
        </a></li>
      {% endif %}
      {% if author[1].soundcloud %}
        <li><a href="https://soundcloud.com/{{ author[1].soundcloud }}" itemprop="sameAs">
          <i class="fa fa-fw fa-soundcloud" aria-hidden="true"></i> 
          Soundcloud
        </a></li>
      {% endif %}
      {% if author[1].weibo %}
        <li><a href="https://www.weibo.com/{{ author[1].weibo }}" itemprop="sameAs">
          <i class="fa fa-fw fa-weibo" aria-hidden="true"></i> 
          Weibo
        </a></li>
      {% endif %}
      {% if author[1].flickr %}
        <li><a href="https://www.flickr.com/{{ author[1].flickr }}" itemprop="sameAs">
          <i class="fa fa-fw fa-flickr" aria-hidden="true"></i> 
          Flickr
        </a></li>
      {% endif %}
      {% if author[1].codepen %}
        <li><a href="https://codepen.io/{{ author[1].codepen }}" itemprop="sameAs">
          <i class="fa fa-fw fa-codepen" aria-hidden="true"></i> 
          CodePen
        </a></li>
      {% endif %}
      {% if author[1].vine %}
        <li><a href="https://vine.co/u/{{ author[1].vine }}" itemprop="sameAs">
          <i class="fa fa-fw fa-vine" aria-hidden="true"></i> 
          Vine
        </a></li>
      {% endif %}
    </ul>
  </div>
</div>
<hr>
{% endfor %}
