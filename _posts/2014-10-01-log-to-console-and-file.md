---
layout: article
permalink: /log-to-console-and-file
title: "Log to both the console and a file"
---
For our Docker containers I wanted the option of logging both to the console and to a file.  And I also wanted to control where the file goes.

1. Install the logging Gem

2. Configure the config/application.rb like so.

{% highlight ruby %}
require 'logging'

class Application < Rails::Application
  
  config.logger = Logging.logger['rails']
  config.logger.add_appenders(
    Logging.appenders.stdout,
    if ENV['LOG_PATH'].present?
      Logging.appenders.file(ENV['LOG_PATH']+'/'+ENV['RAILS_ENV']+'.log')
    else
      Logging.appenders.file('log/'+ENV['RAILS_ENV']+'.log')
    end
  )
  config.logger.level = :debug
{% endhighlight %}

Add LOG_PATH environment variable to your docker run command
