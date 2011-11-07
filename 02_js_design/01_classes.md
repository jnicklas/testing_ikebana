!SLIDE purple

# JavaScript Design

!SLIDE

## It's not really about testing

!SLIDE code small

## Have you written something like this:

    @@@javascript
    $('#whiskies li').each(function() {
      var li = $(this);
      var price = li.attr('data-price');
      var addLink = $('<a class="add-to-cart" href="#">Add to cart</a>');
      addLink.appendTo(li);

      addLink.click(function() {
        var item = $('<li>' + li.attr('data-name') + '</li>');
        item.appendTo('#cart .list');
        item.append('<span class="price">' + price + '</span>');
        var currentAmount = parseInt($('#cart .total .amount').text());
        var newAmount = currentAmount + parseInt(price);
        $('#cart .total .amount').text(newAmount);
        return false;
      });
    });

!SLIDE

# This does not scale!

!SLIDE

# Unstructured
# Untestable

!SLIDE

![John Resig](resig.png)
# It's all jQuery's fault

!SLIDE

## ”jQuery is a fast and concise JavaScript Library that simplifies HTML document traversing, event handling, animating, and Ajax interactions for rapid web development.”

!SLIDE

# jQuery is a DSL for DOM manipultion
## (and it's brilliand at that)

!SLIDE

# jQuery is not your design
## (it doesn't claim to be)

!SLIDE

# We need something more!

!SLIDE

# Structure code into units

!SLIDE blue

# Possible solutions
## Functions
## JS prototypes
## MooTools Classes
## CoffeeScript Classes
## Backbone.js
## Spine.js
## SproutCore

!SLIDE

# Distinct logical units
## which can be tested in isolation

!SLIDE

# Structure application into concerns

!SLIDE

# SRP
## Single Responsibility Principle

!SLIDE

## Every class/unit
# should have one single responsibility

!SLIDE

## We are totally
# ignoring this

!SLIDE code small

# Let's look at this again

    @@@javascript
    $('#whiskies li').each(function() {
      var li = $(this);
      var price = li.attr('data-price');
      var addLink = $('<a class="add-to-cart" href="#">Add to cart</a>');
      addLink.appendTo(li);

      addLink.click(function() {
        var item = $('<li>' + li.attr('data-name') + '</li>');
        item.appendTo('#cart .list');
        item.append('<span class="price">' + price + '</span>');
        var currentAmount = parseInt($('#cart .total .amount').text());
        var newAmount = currentAmount + parseInt(price);
        $('#cart .total .amount').text(newAmount);
        return false;
      });
    });

!SLIDE

* Business logic
* Rendering
* Event handling
* Boostrapping
* (Persistence)

!SLIDE

# Separate concerns
## should be handled separately

!SLIDE

# How?

!SLIDE

# It's up to you!

!SLIDE

# Suggestion: MVC

!SLIDE

# Model

* Persistence
* Business logic

!SLIDE

# Controller

* Event handling

!SLIDE

# View

* Rendering

!SLIDE

# Use a framework

* Backbone.js
* Spine.js
* SproutCore
