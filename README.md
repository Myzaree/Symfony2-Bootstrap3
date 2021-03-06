Symfony2-Bootstrap3
===================

BootstrapBundle looks to integrate [Bootstrap 3](http://getbootstrap.com/) with a Symfony2 v2.4 project. The base implementation hooks into the twig system, overridding the form templates and base html container to use base Bootstrap 3 styles. The Bundle also includes jQuery 1.10.* from a CDN with a local fallback.

Installation
-------------------

Add the project to your composer file.

<dl>
	<dt>composer.json</dt>
	<dd><pre>
{
	"require": {
		"cbc/symfony2-bootstrap": "1.1.*"
	}
}</pre></dd>
</dl>

Add the Bootstrap bundle to AppKernal and include the template.

<dl>
	<dt>/app/AppKernel.php</dt>
	<dd><pre>new CBC\Bundle\BootstrapBundle\BootstrapBundle()</pre></dd>
	<dt>/app/Resources/views/base.html.twig</dt>
	<dd><pre>{% extends 'BootstrapBundle::base.html.twig' %}</pre></dd>
</dl>

Defined Blocks
-------------------

<dl>
	<dt>{% block meta %}</dt>
	<dd>Contains base <meta> html tags.</dd>
	<dt>{% block stylesheets %}</dt>
	<dd>Contains base styles for Bootstrap bundle. Implement {{ parent() }} when overriding.</dd>
	<dt>{% block title %}</dt>
	<dd>Contains the page meta title.</dd>
	<dt>{% block nav %}</dt>
	<dd>Optional block before the content, outside of the container, but inside the wrap.</dd>
	<dt>{% block body %}</dt>
	<dd>Wrapper for the container.</dd>
	<dt>{% block header %}</dt>
	<dd>Adds a header before the content area.</dd>
	<dt>{% block content %}</dt>
	<dd>Base content area inside the container.</dd>
	<dt>{% block footer %}</dt>
	<dd>Optional block after the content, outside the container and wrap.</dd>
	<dt>{% block javascripts %}</dt>
	<dd>Contains base javascript for Bootstrap bundle. Implement {{ parent() }} when overridding.</dd>
</dl>
