# Internationalization for node.js

## Installation

via npm:

    npm install locales

## Usage

    var locales = require('locales'),
        _ = locales.gettext,
        _n = locales.ngettext;

    locales.configure({
      lang: 'zh_CN',
      locales: __dirname + '/locales'
    });

    {{ _("Hello World") }}
    {{ _("Hello {name}", {name: "World"}) }}

    {{ _n("There is a template", "There are {n} templates", 3) }}

    // ./locales/zh_CN.js
    {
      "Hello World": "你好世界",
      "Hello {name}": "你好{name}",
      "There is a template": "有一个模板",
      "There are {n} templates": "有{n}个模板",
    }

    // Within expressjs
    app.use(locales.detector);

## License 

(The MIT License)
