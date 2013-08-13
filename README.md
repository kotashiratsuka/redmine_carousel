# Redmine Carousel Plugin

The plugin can be used for periodic actions that occur during project development process. It automatically generates issue assigned to the next user in the carousel queue every specified time period. You can set users queue, issue settings and time period. Redmine Carousel depends on business_time gem, so you can specify your working hours and holidays, so issues won't be generated if there is nobody in the office.

# Setup

### Dependencies

~~[Business_time](https://github.com/bokmann/business_time) gem is required by Carousel Plugin.~~

~~This gem has a bug that must be fixed to work properly. Detailed explanation [here](https://github.com/bokmann/business_time/issues#issue/4).~~

### Redmine 2.3

Remove Bussiness_time Support.

### Redmine 1.4.x

Use version 1.3.0 or higher.

### Redmine 1.3.x

Use version 1.2.0.

### Redmine < 1.3.x

Use version 1.1.0.

### Plugin installation

Install redmine_carousel into vendor/plugins directory with:

  ruby script/plugin install git@github.com:gmiklaszewski/redmine_carousel.git 

or download and extract tar or zip file.

Run plugins migrations:

  RAILS_ENV=production rake db:migrate_plugins

Restart web server.

Now you can add carousel module to you projects. You can manage carousels in project's settings tab.

### Usage

Put the following rake task in your crontab file:

  RAILS_ENV=production rake carousel:run

Remember to execute it often enough to meet time periods set for you carousels.

# Other stuff

Author:	Grzegorz Miklaszewski <mail@gmiklaszewski.pl>

Contributors:

* Takeshi Kawamoto
* Lubor Nosek

### Warranty

This software is provided "as is" and without any express or implied warranties, including, without limitation, the implied warranties of merchantibility and fitness for a particular purpose.
