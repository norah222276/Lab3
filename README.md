# Lab3
the knowledge: 

male(haif).
male(mufreh).
male(nawaf).
male(mohammed).
male(fahad).
female(alhanouf).
female(sara).
female(reema).
female(norah).
female(rose).
female(hadeel).

parent(haif, alhanouf).
parent(haif, sara).
parent(mufreh, reema).
parent(mufreh, norah).
parent(mufreh, nawaf).
parent(mufreh, rose).
parent(mufreh, hadeel).
parent(mufreh, mohammed).
parent(mufreh, fahad).
parent(alhanouf, reema).
parent(alhanouf, norah).
parent(alhanouf, nawaf).
parent(alhanouf, rose).
parent(alhanouf, hadeel).
parent(alhanouf, mohammed).
parent(alhanouf, fahad).

father(X, Y) :- male(X), parent(X, Y).
mother(X, Y) :- female(X), parent(X, Y).
sister(X, Y) :- female(X), parent(P, X), parent(P, Y), X \= Y.
brother(X, Y) :- male(X), parent(P, X), parent(P, Y), X \= Y.

the queries: 

?- parent(mufreh, reema).
true.

?- parent(alhanouf, nawaf).
true.

?- father(mufreh, rose).
true.

?- mother(alhanouf, hadeel).
true.

?- sister(reema, norah).
true.

?- sister(rose, hadeel).
true.

?- brother(nawaf, mohammed).
true.

?- brother(fahad, reema).
false.









