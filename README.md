
HTTP Header Samples
===================

This is a set of samples of HTTP request and response headers, from browsers
to Web sites. It is intended to inform decisions (including, but not limited
to, header compression) in the design of [HTTP
2.0](http://trac.tools.ietf.org/wg/httpbis/trac/wiki).

Samples are in directories that indicate who generated them, and are named
using the primary Web site that was used to do so. They are in
[HAR](http://www.softwareishard.com/blog/har-12-spec/) format, and can be
viewed using [the HAR viewer](http://s3u.github.com/har-view/).

Caveats
-------

There are an absurd number of caveats to understand when using these traces.

 * They are not representative of the whole Web
 * They are not representative of all browsers
 * They are not representative of all users' interaction patterns
 * They may contain noise in the form of irrelevant requests
 * They may contain invalid terms based on their specific ABNF grammar
   * URIs may have improper/missing point-encoded characters e.g. `%[]{}|`
   * Invalid headers e.g. `Date`, `ETag`, `Server`, `Via`
 * They are a snapshot of how a few Web sites operated at a given time, for 
   a given user

Contributing
------------

If you'd like to add more traces to the sample, please fork this repository,
add a directory with your samples (using your github user name for the
directory name), and make a pull request. 

When contributing, remember to:
  * Turn off as much other software that generates HTTP requests as possible, 
    to limit noise
  * Remove cookies and other PII-containing tokens, or (preferably) use a
    "fresh" browser
  * Do a sanity check on the traces to assure that they're sensible

Any HAR-producing tool can be used. For non-SSL traffic, 
[hdrgrab](https://github.com/mnot/hdrgrab) is preferred, because it records
the headers as they happen "on the wire".


NOTE WELL
=========

Any submission to the [IETF](http://www.ietf.org/) intended by the Contributor
for publication as all or part of an IETF Internet-Draft or RFC and any
statement made within the context of an IETF activity is considered an "IETF
Contribution". Such statements include oral statements in IETF sessions, as
well as written and electronic communications made at any time or place, which
are addressed to:

 * The IETF plenary session
 * The IESG, or any member thereof on behalf of the IESG
 * Any IETF mailing list, including the IETF list itself, any working group 
   or design team list, or any other list functioning under IETF auspices
 * Any IETF working group or portion thereof
 * Any Birds of a Feather (BOF) session
 * The IAB or any member thereof on behalf of the IAB
 * The RFC Editor or the Internet-Drafts function
 * All IETF Contributions are subject to the rules of 
   [RFC 5378](http://tools.ietf.org/html/rfc5378) and 
   [RFC 3979](http://tools.ietf.org/html/rfc3979) 
   (updated by [RFC 4879](http://tools.ietf.org/html/rfc4879)).

Statements made outside of an IETF session, mailing list or other function,
that are clearly not intended to be input to an IETF activity, group or
function, are not IETF Contributions in the context of this notice.

Please consult [RFC 5378](http://tools.ietf.org/html/rfc5378) and [RFC 
3979](http://tools.ietf.org/html/rfc3979) for details.

A participant in any IETF activity is deemed to accept all IETF rules of
process, as documented in Best Current Practices RFCs and IESG Statements.

A participant in any IETF activity acknowledges that written, audio and video
records of meetings may be made and may be available to the public.