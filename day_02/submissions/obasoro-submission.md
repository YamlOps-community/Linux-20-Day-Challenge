 Day 2: Manipulating Text

## Tasks
__Reading:__  
- Chapter 2: Working with Text

### Activity

`sudo cat /etc/logroate.conf`

```
# see "man logrotate" for details

# global options do not affect preceding include directives

# rotate log files weekly
weekly

# keep 4 weeks worth of backlogs
rotate 4

# create new (empty) log files after rotating old ones
create

# use date as a suffix of the rotated file
#dateext

# uncomment this if you want your log files compressed
#compress

# packages drop log rotation information into this directory
include /etc/logrotate.d

# system-specific logs may also be configured here.

```

`sudo nl /etc/logrotate.conf`

```
1  # see "man logrotate" for details

     2  # global options do not affect preceding include directives

     3  # rotate log files weekly
     4  weekly

     5  # keep 4 weeks worth of backlogs
     6  rotate 4

     7  # create new (empty) log files after rotating old ones
     8  create

     9  # use date as a suffix of the rotated file
    10  #dateext

    11  # uncomment this if you want your log files compressed
    12  #compress

    13  # packages drop log rotation information into this directory
    14  include /etc/logrotate.d

    15  # system-specific logs may also be configured here.
    
    ```

    `sudo nl /etc/logrotate.conf | grep logrotate`

    ```
     1  # see "man logrotate" for details
    14  include /etc/logrotate.d

    ```

