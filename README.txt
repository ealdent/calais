Calais
  by Abhay Kumar
  http://opensynapse.net

== DESCRIPTION:
  
A Ruby interface to the Open Calais API (http://opencalais.com)

== FEATURES/PROBLEMS:

* Accepts documents in text/plain, text/xml and text/html format.
* Basic access to the Open Calais API's Enlighten action.
	* Output is RDF representation of input document.
* Single function ability to tag a document and receive a response in RDF format, names in the document, and their relationships.

== SYNOPSIS:

This is a very basic wrapper to the Open Calais API. It uses the POST endpoint and currently supports the Enlighten action. Here's a simple call:

  Calais.enlighten(:content => "The government of the United Kingdom has given corporations like fast food chain McDonald's the right to award high school qualifications to employees who complete a company training program.", :content_type => :text, :license_id => LICENSE_ID)

This is the easiest way to get the RDF-formated response from the OpenCalais service.

If you want to do something more fun like getting all sorts of fun information about a document, you can try this:

  Calais.process_document(:content => "The government of the United Kingdom has given corporations like fast food chain McDonald's the right to award high school qualifications to employees who complete a company training program.", :content_type => :text, :license_id => LICENSE_ID)

This will return an object containing the RDF representation of the text, the names in the text, and any relationships that exist there.

== REQUIREMENTS:

* Ruby 1.8.5 or better
  * Uses the following standard libraries: digest/sha1, net/http, yaml, cgi
* Hpricot

== INSTALL:

TODO

== LICENSE:

(The MIT License)

Copyright (c) 2008 Abhay Kumar

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.