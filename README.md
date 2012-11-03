
HTTP Header Samples
===================

This is a set of samples of HTTP request and response headers, from browsers to Web sites.
It is intended to inform decisions (including, but not limited to, header compression) in the
design of [HTTP 2.0](http://trac.tools.ietf.org/wg/httpbis/trac/wiki).

Samples are in directories that indicate who generated them, and are named using the primary Web
site that was used to do so. They are in [HAR](http://www.softwareishard.com/blog/har-12-spec/) format,
and can be viewed using [the HAR viewer](http://s3u.github.com/har-view/).

Caveats
-------

There are an absurd number of caveats to understand when using these traces.

 * They are not representative of the whole Web
 * They are not representative of all browsers
 * They are not representative of all users' interaction patterns
 * They may contain noise in the form of irrelevant requests
 * They are a snapshot of how a few Web sites operated at a given time, for a given user


Using The Sample
----------------

Eventually, we will have tools to take these files as input and produce a stream of information that can
be used to compare different approaches to problems such as header compression.

Adding To The Sample
--------------------

If you'd like to add more traces to the sample, please fork this repository, add a directory with your samples, and make a pull request. Regular contributors will be added as repository owners to streamline this process.

When contributing, remember to:
  * Turn off as much other software that generates HTTP requests as possible, to limit noise
  * Remove cookies and other PII-containing tokens, or use a "fresh" browser
  * Do a sanity check on the traces to assure that they're sensible

Any HAR-producing tool can be used; e.g., [hdrgrab](https://github.com/mnot/hdrgrab).