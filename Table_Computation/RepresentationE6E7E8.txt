/* This Magma code accompanies the article M.T. Trip - Existence of Minimal del Pezzo Surfaces of Degree 1 with Conic Bundles over Finite Fields.*/

/* It is based on code accompanying the article B. Banwait, F. Fité, D. Loughran - Del Pezzo surfaces over finite fields and their Frobenius traces (see https://sites.google.com/site/danielloughran/publications).*/

/************************** Degree 1 *******************************
*                                                                  *
*******************************************************************/

/* Creates W(E_8) together with its action on the 240 lines of a dP1*/
RD_e8 := RootDatum("E8");
Cox_e8 := CoxeterGroup(RD_e8);
we8 := StandardActionGroup(Cox_e8);

/*This constructs the irreducible representation given by the orthogonal completement of the anticanonical class in the Picard group of the del Pezzo surface.
We work over the large finite field of order 2521 which contains all relevant roots of unity.*/
q := 2521;
AIMwe8 := AbsolutelyIrreducibleModules(we8, FiniteField(q));
Rwe8 := Representation(AIMwe8[4]);
/* To determine the Picard number and trace associated to a type, we want a representation of the action of Galois in GL_2(8).
We see that AIMwe8 contains two modules of dimension 8. A priori I don't know how to choose the correct one, but by comparing the obtained trace values with the values in Urabe we decide that the fourth element of AIMwe8 is the correct representation. */


/************************** Degree 2 *******************************
*                                                                  *
*******************************************************************/

/* Creates W(E_7) together with its action on the 56 lines of a dP2 */
RD_e7 := RootDatum("E7");
Cox_e7 := CoxeterGroup(RD_e7);
we7 := StandardActionGroup(Cox_e7);

/*This constructs the irreducible representation given by the orthogonal completement of the anticanonical class in the Picard group of the del Pezzo surface.
We work over the large finite field of order 2521 which contains all relevant roots of unity.*/
q:=2521;
AIMwe7 := AbsolutelyIrreducibleModules(we7, FiniteField(q));
Rwe7 := Representation(AIMwe7[3]);
/* To determine the Picard number and trace associated to a type, we want a representation of the action of Galois in GL_2(7).
We see that AIMe7 contains two modules of dimension 7. A priori I don't know how to choose the correct one, but by comparing the obtained trace values with the values in Urabe we decide that the third element of AIMe7 is the correct representation. */

/************************** Degree 3 *******************************
*                                                                  *
*******************************************************************/
/* Creates W(E_6) together with its action on the 27 lines of a cubic surface */
RD_e6 := RootDatum("E6");
Cox_e6 := CoxeterGroup(RD_e6);
we6 := StandardActionGroup(Cox_e6);

/*This constructs the irreducible representation given by the orthogonal completement of the anticanonical class in the Picard group of the del Pezzo surface.
We work over the large finite field of order 1801 which contains all relevant roots of unity.*/
q := 1801;
AIMwe6 := AbsolutelyIrreducibleModules(we6, FiniteField(q));
Rwe6 := Representation(AIMwe6[3]);

save "RepresentationE6E7E8";

AIMwe6 := 0;
AIMwe7 := 0;
AIMwe8 := 0;

save "RepresentationE6E7E8_noAIM";
