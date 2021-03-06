.. _type5_ref:

Type 5
======

Type 5 is graphing block that has functional relationship:

.. math::
    F_1(u) = F_2(x,v).


This type of block is used commonly in nomographs that have an equation in form

.. math::
    f_a(a_1,a_2,a_3,...) = f_b(u,v)

and

.. math::
    f_b(u,v)

cannot be represented as line-nomograph. Typically equation above is written as pair of equations:

.. math::
    f_a(a_1,a_2,a_3,...) = x

and

.. math::
    f_b(u,v) = x.

This equation is written in form

.. math::
    F_1(u) = F_2(x,v).

in order to construct this contour block. In reality block consists of horizontal lines:

.. math::
    F_1(u) = y

and contour lines

.. math::
    F_2(x,v) = y,

where x and y are the coordinates of canvas. Coordinate x is reference with name wd in block parameters and it holds

.. math::
    x = f_{wd}(wd).


.. note:: Type 5 is a very complex (say stupid) way to make basic graphs. In the future versions of pynomo a more simple way for graphs will be implemented.

Simple example
--------------
In the following example

.. math::
 F_1(u)=u

and

.. math::
    F_2(wd,v)=wd+v.

Thus the original equation is

.. math::
    wd=u-v.

Generated nomograph
^^^^^^^^^^^^^^^^^^^
.. image:: images/ex_type5_nomo_1.*

Source code of simple example of type 5
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. literalinclude:: ex_codes/ex_type5_nomo_1.py
        :encoding: latin-1
        :linenos:
        :lines: 1-4, 22-


Parameters for type 5
---------------------

Axis parameters
^^^^^^^^^^^^^^^
No specific axis parameters. Everything is defined in block.


Block parameters
^^^^^^^^^^^^^^^^

.. tabularcolumns:: |p{4cm}|p{4cm}|p{7cm}|
.. csv-table:: Specific block parameters for type 5
    :header: "parameter", "default value", "explanation"
    :widths: 10, 10, 60

    "``'block_type'``", "``'type_5'``", "**String.** This is type 5 block."
    "``'width'``", "10.0", "**Float.** Block width (to be scaled)"
    "``'height'``", "10.0", "**Float.** Block height (to be scaled)"
    "``'mirror_x'``", "``False``", "**Boolean.** If x-axis is mirrored"
    "``'mirror_y'``", "``False``", "**Boolean.** If y-axis is mirrored"
    "``'u_func'``", "--", "**func(u).** u function. For example ``lambda u: u``"
    "``'v_func'``", "--", "**func(u,v).** v function. For example ``lambda x,v: x+v``"
    "``'wd_func'``", "--", "**func(wd).** wd func. For example ``lambda wd: wd``"
    "``'wd_func_inv'``", "--", "**func(wd).** Inverse of wd-func. For example ``lambda wd: wd``"
    "``'u_values'``", "--", "**List of Floats.** List of plotted u values. For example `[1.0, 2.0, 3.0, 4.0, 5.0, 6.0, 7.0, 8.0, 9.0, 10.0]``."
    "``'u_tag'``", "``'none'``", "**String.** To align blocks w.r.t each other along axes with same tag."
    "``'u_title'``", "``''``", "**String.** Axis title."
    "``'u_title_x_shift'``", "``0.0``", "**Float.** Title shift in x-direction."
    "``'u_title_y_shift'``", "``0.25``", "**Float.** Title shift in y-direction."
    "``'u_scale_type'``", "``'linear'``", "**String.** Scale type. Can be ``'linear'``: linear scale. ``'log'``: logarithmic scale.  ``'smart linear'``: linear scale with equal spacings.
    ``'smart log'``: logarithmic scale with equal spacings, can also have negative values. ``'manual point'``: Points and corresponding text positions are given manually in ``'manual axis data'``. No line is drawn.
    ``'manual line'``: Ticks and corresponding text positions are given manually in ``'manual axis data'``."
    "``'u_tick_levels'``", "``4``", "**Integer.** How many levels (minor, minor-minor, etc.) of ticks are drawn. Largest effect to 'linear' scale."
    "``'u_tick_text_levels'``", "``'3'``", "**Integer.** How many levels (minor, minor-minor, etc.) of texts are drawn. Largest effect to 'linear' scale."
    "``'u_tick_side'``", "``'right'``", "**String.** Tick and text side in final paper. Can be: ``'right'``or ``'left'``"
    "``'u_reference'``", "``False``", "**Boolean.** If axis is treated as reference line that is a turning point."
    "``'u_reference_padding'``", "``'0.2'``", "**Float.** Fraction of reference line over other lines."
    "``'u_manual_axis_data'``", "``{}``", "**Dict.** Manually set tick/point positions and text positions. Could be for example:``{1:'1', 3.14:r'$\pi$', 5:'5',7:'seven', 10:'10'}`"
    "``'u_title_draw_center'``", "``False``", "**Boolean.** Title is drawn to center of line."
    "``'u_title_distance_center'``", "``'0.5'``", "**Float.** When ``'u_title_draw_center'`` is ``'True'`` sets distance of title from axis."
    "``'u_title_opposite_tick'``", "``True``", "**Boolean.** Title in opposite direction w.r.t ticks."
    "``'u_align_func'``", "``lambda u:u``", "**func(u).** function to align different scales."
    "``'u_align_x_offset'``", "``0.0``", "**Float.** If axis is aligned with other axis, this value x offsets final scale."
    "``'u_align_y_offset'``", "``0.0``", "**Float.** If axis is aligned with other axis, this value y offsets final scale."
    "``'u_text_format'``", "``r'$%4.4g$ '``", "**String.** Format for numbers in scale."
    "``'u_extra_params'``", "``[{},...]``", "**Array of Dicts.** List of dictionary of params to be drawn additionally."
    "``'u_text_distance_#'``", "``x.x``", "**Float.** where #=0,1,2,3 or 4. Distance of text from scale line. Number corresponds to the level, where 0 is the major tick and 4 is the most minor ticks."
    "``'u_grid_length_#'``", "``x.x``", "**Float.** where #=0,1,2,3 or 4. Length of the tick. Number corresponds to the level, where 0 is the major tick and 4 is the most minor ticks."
    "``'u_text_size_#'``", "``x.x``", "**Float.** where #=0,1,2,3 or 4. Text size. For example: ``text.size.small``, ``text.size.scriptsize`` or ``text.size.tiny``. Number corresponds to the level, where 0 is the major tick and 4 is the most minor ticks."
    "``'u_text_size_log_#'``", "``x.x``", "**Float.** where #=0,1 or 2. Text size. For example: ``text.size.small``, ``text.size.scriptsize`` or ``text.size.tiny`` . Number corresponds to the level, where 0 is the major tick and 2 is the most minor ticks."
    "``'u_full_angle'``", "``False``", "**Boolean.** If true, text can be upside down, otherwise +- 90 degrees from horizontal. Good foor example for full circle scales."
    "``'u_extra_angle'``", "``0.0``", "**Float.**  Angle to rotate tick text from horizontal along tick."
    "``'u_text_horizontal_align_center'``", "``False``", "**Boolean.** Aligns tick text horizontally to center. Good when text rotated 90 degrees."
    "``'u_axis_color'``", "``color.rgb.black``", "**Color.** Color of axis."
    "``'u_text_color'``", "``color.rgb.black``", "**Color.** Color of tick texts."
    "``'v_values'``", "--", "**List of Floats.** List of plotted v values. For example `[1.0, 2.0, 3.0, 4.0, 5.0, 6.0, 7.0, 8.0, 9.0, 10.0]``."
    "``'v_title'``", "``''``", "**String.** Axis title."
    "``'v_title_draw_center'``", "``False``", "**Boolean.** Title is drawn to center of line."
    "``'v_title_distance_center'``", "``'0.5'``", "**Float.** When ``'v_title_draw_center'`` is ``'True'`` sets distance of title from axis."
    "``'v_title_opposite_tick'``", "``True``", "**Boolean.** Title in opposite direction w.r.t ticks."
    "``'wd_tag'``", "``'none'``", "**String.** To align blocks w.r.t each other along axes with same tag."
    "``'wd_title'``", "``''``", "**String.** Axis title."
    "``'wd_title_x_shift'``", "``0.0``", "**Float.** Title shift in x-direction."
    "``'wd_title_y_shift'``", "``0.25``", "**Float.** Title shift in y-direction."
    "``'wd_scale_type'``", "``'linear'``", "**String.** Scale type. Can be ``'linear'``: linear scale. ``'log'``: logarithmic scale.  ``'smart linear'``: linear scale with equal spacings.
    ``'smart log'``: logarithmic scale with equal spacings, can also have negative values. ``'manual point'``: Points and corresponding text positions are given manually in ``'manual axis data'``. No line is drawn.
    ``'manual line'``: Ticks and corresponding text positions are given manually in ``'manual axis data'``."
    "``'wd_tick_levels'``", "``4``", "**Integer.** How many levels (minor, minor-minor, etc.) of ticks are drawn. Largest effect to 'linear' scale."
    "``'wd_tick_text_levels'``", "``'3'``", "**Integer.** How many levels (minor, minor-minor, etc.) of texts are drawn. Largest effect to 'linear' scale."
    "``'wd_tick_side'``", "``'right'``", "**String.** Tick and text side in final paper. Can be: ``'right'``or ``'left'``"
    "``'wd_reference'``", "``False``", "**Boolean.** If axis is treated as reference line that is a turning point."
    "``'wd_reference_padding'``", "``'0.2'``", "**Float.** Fraction of reference line over other lines."
    "``'wd_manual_axis_data'``", "``{}``", "**Dict.** Manually set tick/point positions and text positions. Could be for example:``{1:'1', 3.14:r'$\pi$', 5:'5', 7:'seven', 10:'10'}``"
    "``'wd_title_draw_center'``", "``False``", "**Boolean.** Title is drawn to center of line."
    "``'wd_title_distance_center'``", "``'0.5'``", "**Float.** When ``'wd_title_draw_center'`` is ``'True'`` sets distance of title from axis."
    "``'wd_title_opposite_tick'``", "``True``", "**Boolean.** Title in opposite direction w.r.t ticks."
    "``'wd_align_func'``", "``lambda u:u``", "**func(u).** function to align different scales."
    "``'wd_align_x_offset'``", "``0.0``", "**Float.** If axis is aligned with other axis, this value x offsets final scale."
    "``'wd_align_y_offset'``", "``0.0``", "**Float.** If axis is aligned with other axis, this value y offsets final scale."
    "``'wd_text_format'``", "``r'$%4.4g$ '``", "**String.** Format for numbers in scale."
    "``'wd_extra_params'``", "``[{},...]``", "**Array of Dicts.** List of dictionary of params to be drawn additionally."
    "``'wd_text_distance_#'``", "``x.x``", "**Float.** where #=0,1,2,3 or 4. Distance of text from scale line. Number corresponds to the level, where 0 is the major tick and 4 is the most minor ticks."
    "``'wd_grid_length_#'``", "``x.x``", "**Float.** where #=0,1,2,3 or 4. Length of the tick. Number corresponds to the level, where 0 is the major tick and 4 is the most minor ticks."
    "``'wd_text_size_#'``", "``x.x``", "**Float.** where #=0,1,2,3 or 4. Text size. For example: ``text.size.small``, ``text.size.scriptsize`` or ``text.size.tiny``. Number corresponds to the level, where 0 is the major tick and 4 is the most minor ticks."
    "``'wd_text_size_log_#'``", "``x.x``", "**Float.** where #=0,1 or 2. Text size. For example: ``text.size.small``, ``text.size.scriptsize`` or ``text.size.tiny`` . Number corresponds to the level, where 0 is the major tick and 2 is the most minor ticks."
    "``'wd_full_angle'``", "``False``", "**Boolean.** If true, text can be upside down, otherwise +- 90 degrees from horizontal. Good foor example for full circle scales."
    "``'wd_extra_angle'``", "``0.0``", "**Float.**  Angle to rotate tick text from horizontal along tick."
    "``'wd_text_horizontal_align_center'``", "``False``", "**Boolean.** Aligns tick text horizontally to center. Good when text rotated 90 degrees."
    "``'wd_axis_color'``", "``color.rgb.black``", "**Color.** Color of axis."
    "``'wd_text_color'``", "``color.rgb.black``", "**Color.** Color of tick texts."
    "``'horizontal_guides'``", "``False``","**Boolean.** When ``'True'`` generates horizontal guide lines."
    "``'horizontal_guide_nr'``", "``?``","**Float.** When ``'horizontal_guides'`` is ``'True'`` generates ``'n'`` evenly space horizontal guide lines."
    "``'vertical_guides'``", "``True``","**Boolean.** When ``'True'`` generates vertical guide lines."
    "``'vertical_guide_nr'``", "``?``","**Float.** When ``'vertical_guides'`` is ``'True'`` generates ``'n'`` evenly space vertical guide lines."
    "``'isopleth_values'``", "``[[]]``", "** List of list of isopleth values.** Unknown values are given with strings, e.g. 'x'. An example:``[[0.8,'x',0.7],[0.7,0.8,'x']]`` "




General parameters
^^^^^^^^^^^^^^^^^^

See :ref:`main_params` for top level main parameters.