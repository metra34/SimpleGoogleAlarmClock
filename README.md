alarm_clock.py 
===========

An alarm clock that syncs with Google Calendar, written in Python.

#### Features
The alarm dates are read from Google Calendar, any event with the text **wake** will be fetched and its alarm date stored locally. 

#### Requirements

It needs the following libraries installed on your Raspberry Pi:

* [Google Data Library](https://developers.google.com/gdata/articles/python_client_lib#linux)
* [APScheduler](http://pythonhosted.org/APScheduler/#installing-apscheduler)
* PyFeed:
> wget http://sourceforge.net/projects/salix-sbo/files/13.37/pyfeed/pyfeed-0.7.4.tar.gz
> tar -zxvf pyfeed-0.7.4.tar.gz
> cd pyfeed-0.7.4
> sudo python setup.py install
* xe:
> wget http://sourceforge.net/projects/salix-sbo/files/13.37/xe/xe-0.7.4.tar.gz
> tar -zxvf xe-0.7.4.tar.gz
> cd xe-0.7.4.tar.gz
> sudo python setup.py install
* mpg321:
> sudo apt-get install -y mpg321

NOTE: If you’ve never used sound playback on your Raspberry, head [HERE](http://www.raspberrypi-spy.co.uk/2013/06/raspberry-pi-command-line-audio/) for instructions.

#### Howto use
* Copy (git clone) all provided files into a new directory. 
* Edit the config lines *calendar_service.email* and *calendar_service.password* with your google credentials. 
* If you’re using [2-step verification](http://www.google.com/intl/en-GB/landing/2step/), first you need to generate an [application-specific password](https://support.google.com/accounts/answer/185833). 
* The alarm clock can be started by running the command:
> python wakeup.py
or to run it in background:
> nohup python wakeup.py &

#### Todo
Clean up the code. 
Seriously! It is a mess. 
My excuse? These are my first few lines of Python, ever. ;)