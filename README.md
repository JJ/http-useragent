LWP::UserAgent
=============

Basics of Web user agent class for Perl 6.



SYNOPSIS
========

    use LWP::UserAgent;

    my $ua = LWP::UserAgent.new;
    $ua.timeout(10);

    my $response = $ua.get("URL");

    if $response.is_success {
        print $response.content;
    } else {
        die $response.status_line;
    }




INFO (in progress...)
=====================

Constructors
------------

* new(
    parse_head,
    protocols_allowed, \# for now only HTTP
    max_redirect,
    timeout
)
    creates a LWP::UserAgent object

* clone()
    returns a copy of LWP::UserAgent object



Request methods
---------------

* get($url)
    GET request.
