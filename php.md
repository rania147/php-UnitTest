# Test

Automation which is demanding across the globe today saves human time
and energy to a great extent. PHP tools are used to test unit as well as
an end-to-end testing using BDD (Behavior- Driven Development) and TDD
(Test- Driven Development).

Turning now to the implementation of test in the project, we will choose
to make tests for the PHP project because our company Medianet use PHP
language in the development of projects.

The most type of CI test that we need in these projects are:

-   Unit test

-   Static test

-   Integration test

# Unit test:

Starting with unit tests, there are three ways for the implementation of
these tests:

-   TDD -test driven development (tests state -write tests first, then
    write code

-   BDD -behavior driven development (test behavior of the software)

-   ATDD -acceptance test driven development

# Unit test using git:

These are the tasks we require to do our first unit test.

## task 1: show the test code

2 methods exist:

-   Get the code from git so we have to install git

![](media/image1.png)

-   Create a directory where we find the test code

![](media/image2.png)

##task 2: install the plugins that we need

We select git push then press download now and install after restart

![](media/image3.png)

So, this figure appears

![](media/image4.png)

## task 3: create and configure a job

![](media/image5.png)

Then, we press the buttons save, and finally build now

![](media/image6.png)

## task 4: test if it works

This figure \"console output\" shows all the details about the test; if
the test doesn\'t work, we can get all the details right here to fix the
problem![](media/image7.png)

#Unit test using bitbucket:

## What is bitbucket?

Bitbucket is a Git-based source code repository hosting service owned by
Atlassian. Bitbucket offers both commercial plans and free accounts with
an unlimited number of private repositories.

## Task 1: install bitbuckets plugins

We do the same thing we do when installing git plugins.

![](media/image8.png)

## Task 2: create and configure a job

We click on "new item" in the dashboard of Jenkins then we give the name
of the project "my-Bitbucket-project" and choose the option "freestyle
project", this figure represents the next step:

![](media/image9.png)

![](media/image10.png)

Then press "build now" button

![](media/image11.png)

This figure represents dashboard of Jenkins, and it shows the status of
the build: success

![](media/image12.png)

As I know Medianet is a company that uses PHP to program their code so
we need to run tests on these codes using phpunit test.

## PHP unit test (calculator):

Try to execute a PHP unit test using Vs code of a calculator

## Task 1: install needs

### Install Vs code

Install dependencies of vs code in the Virtual machine

![](media/image13.png)
Go to the directory of the dependencies:

\$ cd "/home/rania/Downoads/code_1.69.2-1658162013_amd64"

![](media/image14.png)

Install vs code throw this command

\$ dpkg -i code_1.69.2-1658162013_amd64

![](media/image15.png)

Then in the search box type vs code

![](media/image16.png)

### install phpunit

\$ sudo apt-get -y install phpunit

![](media/image17.png){width="6.3in" height="1.8798611111111112in"}

### install PHP composer

We go to the folder where the code of the calculator existe and run the
following command

\$ curl -sS <https://getcomposer.org/installer> \| php

![](media/image18.png)

Then to verify composer version type

\$ composer --version

![](media/image19.png){width="5.683825459317585in"
height="0.5667158792650918in"}

## Step 2: import the dependencies for PHP unit

\$ composer require phpunit/phpunit \^9

![](media/image20.png)
So, the vendor directory is created automatically

![](media/image21.png)

Version of PHP unit :

*\$ ./vendor/bin/phpunit --version*

![](media/image22.png)

## Step 3: create of the files

### create the xml file

We created a new file called phpunit.xml, then we try this command
''./vendor/bin/phpunit '' to verify that there is no test execute

![](media/image23.png)

### create the PHPunit test file

We add a folder « test », then a file named « CalculatorTest »

![](media/image24.png)

## Step 4: test the code

In the composer.json file, we enter the script shown in the figure
below, then we update the composer

![](media/image25.png)

Finally, we run the command "./vendor/bin/phpunit"; Here I found the
result of the test with the time consumed and the memory
measured![](media/image26.png)

And in this directory, I put the project containing all the previous
files https://github.com/rania147/php_calculator
