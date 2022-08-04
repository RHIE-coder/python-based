# Getting Started

 - [Go To Site](https://www.mkdocs.org/getting-started/)

<br>

# Basic Command

 - mkdocs new [dir-name] - Create a new project.
 - mkdocs serve - Start the live-reloading docs server.
 - mkdocs build - Build the documentation site.
 - mkdocs -h - Print help message and exit.

<br>

# Converting to PDF [ERROR]

[mkdocs with pdf](https://github.com/orzih/mkdocs-with-pdf)

## ERROR STACK LOG

```
INFO     -  Cleaning site directory
INFO     -  Building documentation to directory: ~/githubs/python-based/mkdocs/my-project/site
INFO     -  Number headings up to level 3.
INFO     -  Generate a table of contents up to heading level 2.
INFO     -  Generate a cover page.
Traceback (most recent call last):
  File "/usr/lib/python3.6/runpy.py", line 193, in _run_module_as_main
    "__main__", mod_spec)
  File "/usr/lib/python3.6/runpy.py", line 85, in _run_code
    exec(code, run_globals)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/mkdocs/__main__.py", line 236, in <module>
    cli()
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/click/core.py", line 1128, in __call__
    return self.main(*args, **kwargs)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/click/core.py", line 1053, in main
    rv = self.invoke(ctx)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/click/core.py", line 1659, in invoke
    return _process_result(sub_ctx.command.invoke(sub_ctx))
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/click/core.py", line 1395, in invoke
    return ctx.invoke(self.callback, **ctx.params)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/click/core.py", line 754, in invoke
    return __callback(*args, **kwargs)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/mkdocs/__main__.py", line 192, in build_command
    build.build(config.load_config(**kwargs), dirty=not clean)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/mkdocs/commands/build.py", line 317, in build
    config['plugins'].run_event('post_build', config=config)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/mkdocs/plugins.py", line 104, in run_event
    result = method(**kwargs)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/mkdocs_with_pdf/plugin.py", line 83, in on_post_build
    self.generator.on_post_build(config, self.config['output_path'])
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/mkdocs_with_pdf/generator.py", line 96, in on_post_build
    render = html.render()
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/weasyprint/__init__.py", line 136, in render
    optimize_size, font_config, counter_style, image_cache)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/weasyprint/document.py", line 930, in _render
    [Page(page_box) for page_box in page_boxes],
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/weasyprint/document.py", line 930, in <listcomp>
    [Page(page_box) for page_box in page_boxes],
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/weasyprint/layout/__init__.py", line 133, in layout_document
    pages = list(make_all_pages(context, root_box, html, pages))
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/weasyprint/layout/page.py", line 855, in make_all_pages
    page, resume_at = remake_page(i, context, root_box, html)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/weasyprint/layout/page.py", line 794, in remake_page
    page_state)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/weasyprint/layout/page.py", line 593, in make_page
    discard=False)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/weasyprint/layout/block.py", line 58, in block_level_layout
    page_is_empty, absolute_boxes, fixed_boxes, adjoining_margins, discard)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/weasyprint/layout/block.py", line 73, in block_level_layout_switch
    discard)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/weasyprint/layout/block.py", line 114, in block_box_layout
    absolute_boxes, fixed_boxes, adjoining_margins, discard)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/weasyprint/layout/block.py", line 646, in block_container_layout
    next_page)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/weasyprint/layout/block.py", line 452, in _in_flow_layout
    fixed_boxes, adjoining_margins, discard)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/weasyprint/layout/block.py", line 58, in block_level_layout
    page_is_empty, absolute_boxes, fixed_boxes, adjoining_margins, discard)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/weasyprint/layout/block.py", line 73, in block_level_layout_switch
    discard)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/weasyprint/layout/block.py", line 114, in block_box_layout
    absolute_boxes, fixed_boxes, adjoining_margins, discard)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/weasyprint/layout/block.py", line 646, in block_container_layout
    next_page)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/weasyprint/layout/block.py", line 452, in _in_flow_layout
    fixed_boxes, adjoining_margins, discard)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/weasyprint/layout/block.py", line 58, in block_level_layout
    page_is_empty, absolute_boxes, fixed_boxes, adjoining_margins, discard)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/weasyprint/layout/block.py", line 79, in block_level_layout_switch
    page_is_empty, absolute_boxes, fixed_boxes)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/weasyprint/layout/flex.py", line 159, in flex_layout
    parent_box, page_is_empty, [], [], [], False)[0]
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/weasyprint/layout/block.py", line 58, in block_level_layout
    page_is_empty, absolute_boxes, fixed_boxes, adjoining_margins, discard)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/weasyprint/layout/block.py", line 73, in block_level_layout_switch
    discard)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/weasyprint/layout/block.py", line 114, in block_box_layout
    absolute_boxes, fixed_boxes, adjoining_margins, discard)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/weasyprint/layout/block.py", line 646, in block_container_layout
    next_page)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/weasyprint/layout/block.py", line 452, in _in_flow_layout
    fixed_boxes, adjoining_margins, discard)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/weasyprint/layout/block.py", line 58, in block_level_layout
    page_is_empty, absolute_boxes, fixed_boxes, adjoining_margins, discard)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/weasyprint/layout/block.py", line 73, in block_level_layout_switch
    discard)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/weasyprint/layout/block.py", line 114, in block_box_layout
    absolute_boxes, fixed_boxes, adjoining_margins, discard)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/weasyprint/layout/block.py", line 635, in block_container_layout
    draw_bottom_decoration)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/weasyprint/layout/block.py", line 304, in _linebox_layout
    for i, (line, resume_at) in enumerate(lines_iterator):
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/weasyprint/layout/inline.py", line 45, in iter_line_boxes
    containing_block, absolute_boxes, fixed_boxes, first_letter_style)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/weasyprint/layout/inline.py", line 103, in get_next_linebox
    waiting_floats, line_children)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/weasyprint/layout/inline.py", line 743, in split_inline_box
    line_placeholders, child_waiting_floats, line_children))
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/weasyprint/layout/inline.py", line 476, in split_inline_level
    context, box, max_x - position_x, skip)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/weasyprint/layout/inline.py", line 912, in split_text_box
    text, box.style, context, available_width, box.justification_spacing)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/weasyprint/text/line_break.py", line 355, in split_first_line
    text, style, context, original_max_width, justification_spacing)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/weasyprint/text/line_break.py", line 291, in create_layout
    context, style['font_size'], style, justification_spacing, max_width)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/weasyprint/text/line_break.py", line 84, in __init__
    self.setup(context, font_size, style)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/weasyprint/text/line_break.py", line 100, in setup
    pango.pango_context_set_round_glyph_positions(pango_context, False)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/cffi/api.py", line 912, in __getattr__
    make_accessor(name)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/cffi/api.py", line 908, in make_accessor
    accessors[name](name)
  File "~/githubs/python-based/mkdocs/my-project/tester/lib/python3.6/site-packages/cffi/api.py", line 838, in accessor_function
    value = backendlib.load_function(BType, name)
AttributeError: function/symbol 'pango_context_set_round_glyph_positions' not found in library 'libpango-1.0.so.0': /usr/lib/x86_64-linux-gnu/libpango-1.0.so.0: undefined symbol: pango_context_set_round_glyph_positions
```