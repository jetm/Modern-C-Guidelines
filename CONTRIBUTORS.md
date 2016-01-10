### Contributors

Jeremy Faller and [Sos
Sosowski](https://twitter.com/Sosowski/status/685431663501926400) and Martin
Heistermann and a few other people were kind enough to point out my `memset()`
example was broken and provided the proper fix.

Martin Heistermann also pointed out the `localThing = localThingNull` example
was broken.

The opening quote about not writing C if you can avoid it is from the wise
internet sage [\@badboy\_](https://twitter.com/badboy\_).

[Remi Gacogne](https://twitter.com/rgacogne/status/685390620723154944) pointed
out I forgot `-Wextra`.

[Levi Pearson](https://twitter.com/pineal_servo/status/685393454487056384)
pointed out gcc-5 defaults to gnu11 instead of c89 as well as clarifying the
default clang mode.

[Christopher](https://twitter.com/shrydar/status/685375992114757632) pointed
out the `-O2` vs `-O3` section could use a little more clarification.

[Chad Miller](https://twitter.com/chadmiller/status/685469896914919424) pointed
out I was being lazy in the clang-format script params.

[Many](https://twitter.com/lordcyphar/status/685444198481412096) people also
pointed out the `calloc()` advice isn't *always* a good idea if you have
extreme circumstances or non-standard hardware (examples of bad ideas: huge
allocations, allocations on embedded jiggers, allocations on 30 year old
hardware, etc).

Charles Randolph pointed out I misspelled the world "Building."

Sven Neuhaus pointed out kindly I also do not posess the ability to spell
"initialization" or "initializers." (and also pointed out I misspelled
"initialization" wrong the first time here as well)

[Colm MacCárthaigh](https://twitter.com/colmmacc/status/685493166988906497)
pointed out I forgot to mention `#pragma once`.

[Jeffrey Yasskin](https://twitter.com/jyasskin/status/685493531515826176)
pointed out we should kill strict aliasing too (mainly a gcc optimization).

Jeffery Yasskin also provided better wording around the `-fno-strict-aliasing`
section.

[Chris Palmer](https://twitter.com/fugueish/status/685503534230458369) and a
few others pointed out calloc-vs-malloc parameter advantages and the overall
drawback of writing a wrapper for `calloc()` because `calloc()` provides a more
secure interface than `malloc()` in the first place.

Damien Sorresso pointed out we should remind people `realloc()` doesn't zero
out grown memory after an initial zero'd `calloc()` request.

Pat Pogson pointed out I was unable to spell the word "declare" correctly as
well.

[\@TopShibe](https://twitter.com/TopShibe/status/685505183762223105) pointed
out the stack-allocated initialization example was wrong because the examples I
gave were global variables.  Updated wording to just mean "auto-allocated"
things, be it stack or data sections.

[Jonathan Grynspan](https://twitter.com/grynspan/status/685509158024691712)
suggested harsher wording around the VLA example because they **are** dangerous
when used incorrectly.

David O'Mahony kindly pointed out I can't spell "specify" either.

Dr. David Alan Gilbert pointed out `ssize_t` is a POSIXism and Windows either
doesn't have it or defines `ssize_t` as an *unsigned* quantity which obviously
introduces all kinds of fun behavior when your type is signed on POSIX
platforms and unsigned on Windows.

Chris Ridd suggested we explicitly mention C99 is C from 1999 and C11 is C from
2011 because otherwise it looks strange having 11 be newer than 99.

Chris Ridd also noticed the `clang-format` example used unclear naming
conventions and suggested better consistency across examples.

[Anthony Le Goff](https://twitter.com/Ideo_logiq/status/685384708188930048)
pointed us to a book-length treatment of many modern C ideas called [Modern
C](http://icube-icps.unistra.fr/img_auth.php/d/db/ModernC.pdf).

Stuart Popejoy pointed out my inaccurate spelling of deliberately was truly
inaccurate.

Jack Rosen pointed out my usage of the word 'exists' does not mean 'exits' as I
intended.

Jo Booth pointed out I like to spell compatibility as compatability, which
seems more logical, but English commonality disagrees.

Stephen Anderson decoded my aberrant spelling of 'stil' back into 'still.'

Richard Weinberger pointed out struct initialization with `{0}` doesn't zero
out padding bytes, so sending a `{0}` struct over the wire can leak unintended
bytes on under-specified structs.

[\@JayBhukhanwala](https://twitter.com/JayBhukhanwala) pointed out the function
comment in [Return Parameter Types](#return-parameter-types) was inaccurate
because I didn't update the comment when the code changed (story of our lives,
right?).
