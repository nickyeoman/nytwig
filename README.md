# Nix Twig Templates

This is the scaffolding Nick uses for his web projects.  
It is based, but heavly modifed, on html5boilerplate.

* [Github](https://github.com/nickyeoman/nytwig)
* [Packagist](https://packagist.org/packages/nickyeoman/nytwig)

## Installation

You will have to configure your application to include the vendor directory and asssign the namespace "nytwig" (required)

### How To [Twig](https://twig.symfony.com/doc/2.x/api.html#loaders)

```php
$loader->addPath('vendor/nickyeoman/nytwig/src', 'nytwig');
```

### How To [Symfony](https://symfony.com/doc/current/templates.html#template-namespaces)

Open the file ```config/packages/twig.yaml``` and add (under "default_path"):

```yaml
paths:
    '%kernel.project_dir%/vendor/nickyeoman/nytwig/src': 'nytwig'
```

## Use

```twig
{% extends '@nytwig/master.html.twig' %}

{% block body %}
<p>Content Here</p>
{% endblock %}
```

## Overrides

In your view directly create a folder named 'cms' and create the file you want to override there with the same name.