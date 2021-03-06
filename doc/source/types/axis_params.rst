

.. tabularcolumns:: |p{4cm}|p{4cm}|p{7cm}|
.. csv-table:: Common axis params
    :header: "parameter", "default value", "explanation"
    :widths: 10, 10, 40

    "``'ID'``", "``'none'``", "**String.** To identify the axis."
    "``'tag'``", "``'none'``", "**String.** To align blocks w.r.t each other along axes with same tag."
    "``'dtag'``", "``'none'``", "**String.** To double-align blocks w.r.t each other along axes with same tag."
    "``'title'``", "``''``", "**String.** Axis title."
    "``'title_x_shift'``", "``0.0``", "**Float.** Title shift in x-direction."
    "``'title_y_shift'``", "``0.25``", "**Float.** Title shift in y-direction."
    "``'scale_type'``", "``'linear'``", "**String.** Scale type. Can be ``'linear'``: linear scale. ``'log'``: logarithmic scale.  ``'smart linear'``: linear scale with equal spacings.
    ``'smart log'``: logarithmic scale with equal spacings, can also have negative values. ``'manual point'``: Points and corresponding text positions are given manually in ``'manual axis data'``. No line is drawn.
    ``'manual line'``: Ticks and corresponding text positions are given manually in ``'manual axis data'``."
    "``'tick_levels'``", "``4``", "**Integer.** How many levels (minor, minor-minor, etc.) of ticks are drawn. Largest effect to 'linear' scale."
    "``'tick_text_levels'``", "``'3'``", "**Integer.** How many levels (minor, minor-minor, etc.) of texts are drawn. Largest effect to 'linear' scale."
    "``'tick_side'``", "``'right'``", "**String.** Tick and text side in final paper. Can be: ``'right'`` or ``'left'``."
    "``'reference'``", "``False``", "**Boolean.** If axis is treated as reference line that is a turning point."
    "``'reference_padding'``", "``'0.2'``", "**Float.** Fraction of reference line over other lines."
    "``'manual_axis_data'``", "``{}``", "**Dict.** Manually set tick/point positions and text positions. Could be for example:``{1:'1', 3.14:r'$\pi$', 5:'5', 7:'seven', 10:'10'}``"
    "``'title_draw_center'``", "``False``", "**Boolean.** Title is drawn to center of line."
    "``'title_distance_center'``", "``'0.5'``", "**Float.** When ``'title_draw_center'`` is ``'True'`` sets distance of title from axis."
    "``'title_opposite_tick'``", "``True``", "**Boolean.** Title in opposite direction w.r.t ticks."
    "``'align_func'``", "``lambda u:u``", "**func(u).** function to align different scales."
    "``'align_x_offset'``", "``0.0``", "**Float.** If axis is aligned with other axis, this value x offsets final scale."
    "``'align_y_offset'``", "``0.0``", "**Float.** If axis is aligned with other axis, this value y offsets final scale."
    "``'text_format'``", "``r'$%4.4g$ '``", "**String.** Format for numbers in scale."
    "``'extra_params'``", "``[{},...]``", "**Array of Dicts.** List of dictionary of params to be drawn additionally."
    "``'text_distance_#'``", "``x.x``", "**Float.** where #=0,1,2,3 or 4. Distance of text from scale line. Number corresponds to the level, where 0 is the major tick and 4 is the most minor ticks."
    "``'grid_length_#'``", "``x.x``", "**Float.** where #=0,1,2,3 or 4. Length of the tick. Number corresponds to the level, where 0 is the major tick and 4 is the most minor ticks."
    "``'text_size_#'``", "``x.x``", "Where #=0,1,2,3 or 4. Text size for linear scale specified by parameter. For example: ``text.size.small``, ``text.size.scriptsize`` or ``text.size.tiny``. Number corresponds to the level, where 0 is the major tick and 4 is the most minor ticks."
    "``'text_size_log_#'``", "``x.x``", "Where #=0,1 or 2. Text size for log scale specified by parameter. For example: ``text.size.small``, ``text.size.scriptsize`` or ``text.size.tiny`` . Number corresponds to the level, where 0 is the major tick and 2 is the most minor ticks."
    "``'full_angle'``", "``False``", "**Boolean.** If true, text can be upside down, otherwise +- 90 degrees from horizontal. Good foor example for full circle scales."
    "``'extra_angle'``", "``0.0``", "**Float.**  Angle to rotate tick text from horizontal along tick."
    "``'text_horizontal_align_center'``", "``False``", "**Boolean.** Aligns tick text horizontally to center. Good when text rotated 90 degrees."
    "``'turn_relative'``", "``False``", "**Boolean.** Side left or right is relative according to traveling of scale from min to max."
    "``'arrow_size'``", "``0.2``", "**Float.** Used with arrow scale."
    "``'arrow_length'``", "``1.0``", "**Float.** Used with arrow scale.."
    "``'arrow_color'``", "``color.rgb.black``", "**Color.** Used with arrow scale."
    "``'axis_color'``", "``color.rgb.black``", "**Color.** Color of axis."
    "``'text_color'``", "``color.rgb.black``", "**Color.** Color of tick texts."
    "``'extra_titles'``", "``[]``", "**Array.** List of extra title dicts for scale. Could be i.e.``[{'dx':1.0, 'dy':1.0, 'text':'extra title 1', 'width':5, 'pyx_extra_defs': [color.rgb.red,text.size.Huge]}, {'text': 'extra title 2'}]``."
    "``'base_start'``", "``None``", "**None/Float.** Defines number with ``'base_stop'`` (instead of ``'u_min'`` or ``'u_max'``) to find major tick decades."
    "``'base_stop'``", "``None``", "**None/Float.** Defines number with ``'base_start'`` (instead of ``'u_min'`` or ``'u_max'``) to find major tick decades."
    "``'tick_distance_smart'``", "``.05``", "**Float**. Minimum distance between smart ticks."
    "``'text_distance_smart'``", "``.25``", "**Float**. Minimum distance between smart texts."

