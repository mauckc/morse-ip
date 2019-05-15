# morse-ip
Enable IoT devices to easily display their IP address using Morse Code

## Network
Parse ifconfig reponse or ipconfig

### Unix/Linux and Mac OS

The following command was runs ifconfig on en0
```shell
/sbin/ifconfig en0 | grep inet\ | awk '{print $2}'
```
Returns
```
10.0.0.171
```

## Morse Dictionary
```python3
CODE = {' ': ' ', 
        "'": '.----.', 
        '(': '-.--.-', 
        ')': '-.--.-', 
        ',': '--..--', 
        '-': '-....-', 
        '.': '.-.-.-', 
        '/': '-..-.', 
        '0': '-----', 
        '1': '.----', 
        '2': '..---', 
        '3': '...--', 
        '4': '....-', 
        '5': '.....', 
        '6': '-....', 
        '7': '--...', 
        '8': '---..', 
        '9': '----.', 
        ':': '---...', 
        ';': '-.-.-.', 
        '?': '..--..', 
        'A': '.-', 
        'B': '-...', 
        'C': '-.-.', 
        'D': '-..', 
        'E': '.', 
        'F': '..-.', 
        'G': '--.', 
        'H': '....', 
        'I': '..', 
        'J': '.---', 
        'K': '-.-', 
        'L': '.-..', 
        'M': '--', 
        'N': '-.', 
        'O': '---', 
        'P': '.--.', 
        'Q': '--.-', 
        'R': '.-.', 
        'S': '...', 
        'T': '-', 
        'U': '..-', 
        'V': '...-', 
        'W': '.--', 
        'X': '-..-', 
        'Y': '-.--', 
        'Z': '--..', 
        '_': '..--.-'}
```     
        
        
### A Few Helpful Tips:

* CODE['Z'] will return '--..', the Morse code for Z
* There are only upper case characters, 'z'.upper() will return 'Z'
* A dot should correspond to the LED being on for about half the time of a dash
* You will want a pause between each character and for a space
* You can get input from a user with raw_input('this is the prompt to be displayed ')
* You can loop through a string one character at a time with

```python3
    for letter in string:
      print(letter)
```



### Resources

https://www.cl.cam.ac.uk/projects/raspberrypi/tutorials/robot/morse_code/
