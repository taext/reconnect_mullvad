
## reconnect_mullvad docs v0.1

View the command-line help with option `-h`


```python
reconnect_mullvad -h
```

    usage: reconnect_mullvad [-h] [-c COUNTRIES] time_in_minutes
    
    Waits for n minutes and then changes Mullvad IP, optionally also country.
    Ctrl-C to change now and restart timer, Ctrl-C twice to exit.
    
    positional arguments:
      time_in_minutes       time to wait in minutes
    
    options:
      -h, --help            show this help message and exit
      -c COUNTRIES, --countries COUNTRIES
                            a string of 2-character country codes to randomly
                            alternate between


###

reconnect_mullvad needs a wait time in minutes argument, here 15 minutes to renew IP (within same country):


```python
reconnect_mullvad 15
```

    Connected to de-fra-wg-103 in Frankfurt, Germany
    Your connection appears to be from: Germany, Frankfurt. IPv4: 146.70.117.240
    
    Waiting 15 minutes ▣▢▢▢▢▢▢▢▢▢▢▢▢▢▢▢▢▢▢▢▢▢▢▢▢▢▢▢▢▢▢▢ 3%

###

add `--countries` option to input a string of two-character country codes to alternate between:


```python
reconnect_mullvad 15 --countries "de se no"
```

    Connected to se-sto-wg-014 in Stockholm, Sweden
    Your connection appears to be from: Sweden, Stockholm. IPv4: 185.195.233.215
    
    Waiting 15 minutes ▢▢▢▢▢▢▢▢▢▢▢▢▢▢▢▢▢▢▢▢▢▢▢▢▢▢▢▢▢▢▢▢ 1%

###

### Note that Ctrl-C has been over-loaded 😃

While the timer is active and counting down, press Ctrl-C once to change IP now and reset timer, Ctrl-C twice to exit.

