# OCAML-PGMS
Programs to show Functional Programming written in OCAML.
Details of pgms are :

PGM-1:
In formal languages, regular expressions (REs) can be dened as follows:
 ; is an RE that does not match any string;
 any string (": : :") is an RE that matches only itself;
 r1r2 is an RE that matches all strings that can be partitioned into two substrings s1 and
s2, such that s1 matches r1 and s2 matches r2;
 r1 + r2 is an RE that matches all strings that match r1 or r2; and
 r (Kleene star) is an RE that matches any string that can be partitioned into n  0
substrings, all of which match r. (Note that r therefore always matches the empty
string, since n can be 0.)

PGM-2:

Dene a global variable named myregexp that models the regular expression
(("hello" + "goodbye")"world"). Your variable should have type rexp.

PGM-3:

Implement a function (isempty r) that returns true if regular expression
r does not match any strings and false otherwise. Your function should have type
isempty : rexp ! bool.

PGM-4:

Implement a function (update f x y) that accepts as input a function f and values
x and y, and returns a new function g that is just like function f except that g(x) = y. Your
function should work properly no matter what types x and y have. For example, if I test your
function by writing
let f s = s ^ "abc";;
let g = (update f "X" "Y");;
then (g "A") should yield "Aabc" but but (g "X") should yield "Y". Your update function
should have the polymorphic type: ('a!'b)!'a!'b!('a!'b)
Hint: A formal mathematical denition of g would look like this:
g(n ) = (y if n = x
         f(n) if n != x
