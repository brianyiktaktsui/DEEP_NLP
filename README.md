
 

### convert the NCIT to terms in phrase matcher 

code: ./NCIT_parsing.ipynb

input: Thesaurus.txt

output: ./Data/NCIT_table.pickle


```python
!jupyter nbconvert --to markdown notebook.ipynb

```

    [NbConvertApp] WARNING | pattern 'notebook.ipynb' matched no files
    Traceback (most recent call last):
      File "/cellar/users/btsui/Data/miniconda3/bin/jupyter-nbconvert", line 11, in <module>
        sys.exit(main())
      File "/cellar/users/btsui/Data/miniconda3/lib/python3.6/site-packages/jupyter_core/application.py", line 266, in launch_instance
        return super(JupyterApp, cls).launch_instance(argv=argv, **kwargs)
      File "/cellar/users/btsui/Data/miniconda3/lib/python3.6/site-packages/traitlets/config/application.py", line 658, in launch_instance
        app.start()
      File "/cellar/users/btsui/Data/miniconda3/lib/python3.6/site-packages/nbconvert/nbconvertapp.py", line 325, in start
        self.convert_notebooks()
      File "/cellar/users/btsui/Data/miniconda3/lib/python3.6/site-packages/nbconvert/nbconvertapp.py", line 482, in convert_notebooks
        cls = get_exporter(self.export_format)
      File "/cellar/users/btsui/Data/miniconda3/lib/python3.6/site-packages/nbconvert/exporters/base.py", line 110, in get_exporter
        % (name, ', '.join(get_export_names())))
    ValueError: Unknown exporter "MD", did you mean one of: asciidoc, custom, html, latex, markdown, notebook, pdf, python, rst, script, slides?

