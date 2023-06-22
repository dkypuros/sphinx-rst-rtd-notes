
## Special Advanced Sphinx Stuff - That I love

### Only Tested with "sphinx_rtd_theme"

_templates/page.html
-----------------------------

{% extends "!page.html" %}

{% block footer %}
 <script type="text/javascript">
    $(document).ready(function() {
        $(".toggle > *").hide();
        $(".toggle .header").show();
        $(".toggle .header").click(function() {
            $(this).parent().children().not(".header").toggle(400);
            $(this).parent().children(".header").toggleClass("open");
        })
    });
</script>
{% endblock %}


_static/custom.css
-------------------------
.toggle .header {
    display: block;
    clear: both;
}

.toggle .header:after {
    content: " ▶";
}

.toggle .header.open:after {
    content: " ▼";
}

conf.py
----------------

def setup(app):
    app.add_css_file('custom.css')

Sphinx page
--------------------------
.. container:: toggle

    .. container:: header

        **Show/Hide Code**

    .. code-block:: xml
       :linenos:

       from plone import api
       ...
