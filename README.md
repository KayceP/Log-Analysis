![Part of the Udacity Front-End Web Development Nanodegree](https://img.shields.io/badge/Udacity-Front--End%20Web%20Developer%20Nanodegree-02b3e4.svg)
> Developed for project 4 of 6 as part of the **Udacity Front-End Web Developer Nanodegree**.

# Logs Analysis

A log analysis program made for the [Udacity Full Stack Nanodegree program](https://www.udacity.com/uconnect/intensive/full-stack-web-developer-nanodegree), with Python.

![screenshot](https://i.imgur.com/sFh5Ucg.png)

## Project Overview

For this project, we were tasked with a scenario where we've been hired onto a team working on a newspaper's website. 

We then were instructed to build an internal program that will analyze the newspaper's raw database to discover:

- What are the most popular three articles of all time?
- Who are the most popular article authors of all time?
- On which days did more than 1% of requests lead to errors?

## Requirements

**[VirtualBox](https://www.virtualbox.org/)**

**[Vagrant](https://www.vagrantup.com/)**

The vagrant file contained within this repository will automatically configure the following, which are listed below for reference. 

- Python3
- SQL Alchemy
- postgresql
- psycopg2
- bleach
- flask
- flask-httpauth
- oauth2client
- requests
- redis
- passlib
- packaging

In addition, empty databases will be created for you in advance, as seen below.

```
    su vagrant -c 'createdb'
    su vagrant -c 'createdb news'
    su vagrant -c 'createdb forum'
    su vagrant -c 'psql forum -f /vagrant/forum/forum.sql'
```

## Configuration

- Install VirtualBox and Vagrant, using the default installation options.
- Open a command terminal (I reccomend [GitBash](https://git-scm.com/downloads)) in the folder you extracted this repository in.
- Bring Vagrant online by executing the following commands in a command terminal. 

```
$ vagrant up
$ vagrant ssh
```
- Information on how to configure the system will be automatically imported from the Vagrantfile.

1. Download the [mock database file](https://d17h27t6h515a5.cloudfront.net/topher/2016/August/57b5f748_newsdata/newsdata.zip).
2. Unzip the file, which will contain 'newsdata.sql'.
3. Place 'newsdata.sql' in the directory you're be using for this program.
4. Populate the data into the pre-prepared databases by executing the command:
```
psql -d news -f newsdata.sql
```

## Running

 - Finally, execute the program by running internal_report_01.py:
```
python3 internal_report_01.py
```
 - Text will be output to the terminal containing the answers to our original questions:

	- What are the most popular three articles of all time?
	- Who are the most popular article authors of all time?
	- On which days did more than 1% of requests lead to errors?

## Credits

Skeleton / base code from Udacity:
  - [Fullstack Nanodegree](https://github.com/udacity/fullstack-nanodegree-vm)
