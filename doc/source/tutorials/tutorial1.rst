Tutorial 1: Vehicle economy calculator
-----------------------

*********
Objective
*********

Construct an "N" type nomogram to calculate a vehicle's range, fuel consumption or fuel economy given any two of these values.  The nomogram will be built using linear scales.

**************************
Nomogram construction
**************************

Nomogram construction involves several steps.  The first is always to identify the variables and their relationship. In this tutorial we need to consider three variables:

* distance (:math:`d`) measured in kilometres,
* fuel consumed (:math:`c`) measured in litres, and
* fuel economy  (:math:`e`) measured in kilometres driven per litre consumed.

The relationship between these variables is:

:math:`d = {e\times c}.`

This equation satisfies the form for a Type 2 nomogram (see section 6.2) as follows:

:math:`F_1(u_1) = {F_2(u_2)F_3(u_3)},`

where

:math:`F_1(u_1) = u_1 = d`,

:math:`F_2(u_2) = u_2 = e`

and

:math:`F_3(u_3) = u_3 = c`.


All scales are linear and we choose a reasonable range of values (:code:`u_min` and :code:`u_max`) for each axis.  

.. literalinclude:: source_code/tutorial1a.py
    :linenos:
    :language: python
    :lineno-start: 11
    :lines: 11-40

These scales are linked into a single block as follows:

.. literalinclude:: source_code/tutorial1a.py
    :linenos:
    :language: python
    :lineno-start: 42
    :lines: 42-47


.. note::
    Parameters :code:`f1_params`, :code:`f2_params` and :code:`f3_params` represent parameters
    including functions for variables :math:`u_1`, :math:`u_2` and :math:`u_3` respectively.

Finally, we define main parameters of the nomogram and generate the chart:

.. literalinclude:: source_code/tutorial1a.py
    :linenos:
    :language: python
    :lineno-start: 49
    :lines: 49-57


**************************
Generated nomogram
**************************

.. image:: images/tutorial1a.*

**************************
A variation on vehicle economy calculator
**************************

The previously generated nomogram is complete but doesn’t express the vehicle’s economy the way we would like.  A vehicle’s fuel economy is more often expressed in litres consumed per 100 kilometres driven, 100 times the reciprocal of the original function.  How do we do this?

Recall that

:math:`d = {e\times c}`

and thus

:math:`{\frac{d}{c}} = e`.

We express the reciprocal of the economy by rearranging the formula as

:math:`\frac{c}{d} = \frac{1}{e}`.

Since our goal is to describe fuel economy in terms of litres per *100 km*
we multiply :math:`\frac{1}{e}` by 100 to achieve the correct units:

:math:`\frac{c}{d} = \frac{100.0}{e}`.

:math:`u_2 = e` so our function for :math:`u_2` becomes

:math:`\frac{100.0}{u_2}`

and we amend the axis definition:

.. literalinclude:: source_code/tutorial1b.py
    :linenos:
    :language: python
    :lineno-start: 21
    :lines: 21-30

**************************
Generated nomogram
**************************

.. image:: images/tutorial1b.*

