wakeup.py 
===========

An alarm clock that syncs with Google Calendar, written in Python.

#### Features
The alarm dates are read from Google Calendar, any event with the text of your choice will be fetched and alarm triggered from console. 

#### Requirements

It needs the following libraries installed on your Raspberry Pi:

* [Google Data Library](https://developers.google.com/gdata/articles/python_client_lib#linux)
* [APScheduler](http://pythonhosted.org/APScheduler/#installing-apscheduler)
* PyFeed:<BR>
can be found in **libs** directory. From the repository dir:<BR>
<code>> cd libs<BR>
> tar -zxvf pyfeed-0.7.4.tar.gz<BR>
> cd pyfeed-0.7.4<BR>
> sudo python setup.py install</code>
* mpg321:
<code>> sudo apt-get install -y mpg321</code>

NOTE: If you’ve never used sound playback on your Raspberry Pi, head [HERE](http://www.raspberrypi-spy.co.uk/2013/06/raspberry-pi-command-line-audio/) for instructions.

#### Howto use
* Copy (git clone) all provided files into a new directory. 
* Edit the config file **wakeup.cfg** with your Google credentials and mp3 path. 
* If you’re using [2-step verification](http://www.google.com/intl/en-GB/landing/2step/), first you need to generate an [application-specific password](https://support.google.com/accounts/answer/185833). 
* The alarm clock can be started by running the command:
<code>> python wakeup.py</code><BR>
or to run it in background:
<code>> nohup python wakeup.py &</code>
* To add alarm at specific time/date, just head to Google Calendar and create an Event with phrase **wake** in the title. The phrase can be easily changed in the config file.
