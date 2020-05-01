# molcajete
A continuous integration framework

[![crates.io](https://img.shields.io/crates/v/molcajete.svg)](https://crates.io/crates/molcajete)
[![Build Status](https://travis-ci.org/molcajete/molcajete.svg?branch=master)](https://travis-ci.org/molcajete/molcajete)

Molcajete receives a task and when a worker is available it will execute it and
report the results.

A task (for now) is an event from a GitHub webhook, the payload gets processed,
and then a task is created, for example, for every commit to the git branches
development or master, a task is created.

Once the worker receives a task it will create a FreeBSD jail and within it will
run all the tasks defined in `molcajete.yml` reporting back the results.