# SocialMedia plugin for CakePHP

[![Build Status](https://travis-ci.org/Oefenweb/cakephp-social-media.png?branch=master)](https://travis-ci.org/Oefenweb/cakephp-social-media)
[![PHP 7 ready](http://php7ready.timesplinter.ch/Oefenweb/cakephp-social-media/badge.svg)](https://travis-ci.org/Oefenweb/cakephp-social-media)
[![Coverage Status](https://codecov.io/gh/Oefenweb/cakephp-social-media/branch/master/graph/badge.svg)](https://codecov.io/gh/Oefenweb/cakephp-social-media)
[![Packagist downloads](http://img.shields.io/packagist/dt/Oefenweb/cakephp-social-media.svg)](https://packagist.org/packages/oefenweb/cakephp-social-media)
[![Code Climate](https://codeclimate.com/github/Oefenweb/cakephp-social-media/badges/gpa.svg)](https://codeclimate.com/github/Oefenweb/cakephp-social-media)
[![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/Oefenweb/cakephp-social-media/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/Oefenweb/cakephp-social-media/?branch=master)

The SocialMedia plugin provides the tools to generate social media links (Helper) and handle them (Controller).

## Requirements

* CakePHP 2.9.0 or greater.
* PHP 7.0.0 or greater.

## Installation

* Clone/Copy the files in this directory into `app/Plugin/SocialMedia`

## Configuration

* Ensure the plugin is loaded in `app/Config/bootstrap.php` by calling:

```
CakePlugin::load('SocialMedia');
```

* Ensure to configure the following two lines in `app/Config/bootstrap.php`:

```
Configure::write('SocialMedia.salt', 'your-salt');
Configure::write('SocialMedia.facebookAppId', 'your-facebook-app-id');
```

## Usage

### Facebook share link

```
echo $this->SocialMedia->facebook(
	__('Share on Facebook'), [
		'link' => 'your-url',
		'name' => 'your-name',
		'caption' => 'your-caption',
		'description' => 'your-description',
		'picture' => 'your-picture'
	]
);
```

### Twitter tweet link

```
echo $this->SocialMedia->twitter(
	__('Tweet on Twitter'), [
		'url' => 'your-url',
		'via' => 'your-via',
		'text' => 'your-text',
	]
);
```
