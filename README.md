# Codeforces Submit

This is a script to automatically submit codes for codeforces problems only with one click of running the script :relaxed:
I made this script because it seems too boring to me to select file of my code by going to that folder through dropdown menu :stuck_out_tongue_winking_eye:

**Currently only for Chrome on Linux** (will update for Windows and Firefox soon )

## Prerequisite

```bash
sudo pip3 install selenium
```

Download chromedriver zip file according to your chrome version (you can check your chrome version on `chrome://version`) from [here](https://sites.google.com/a/chromium.org/chromedriver/downloads).

## Setup configuration

### For initial one time settings

1. Go to `chrome://version` and copy the path given in heading of **profile path** and paste it in place of line:  
   `options.add_argument("user-data-dir=/home/kanish/.config/google-chrome/Default")`
   in both `starter_script.py` and `script.py` file. Mention that profile path instead of `/home/USER/.config/google-chrome/Default`

2. Get path of your chromedriver which you downloaded in pre-requisites and copy it in line :  
   `driver=webdriver.Chrome(executable_path='/home/kanish/Documents/chromedriver/chromedriver',chrome_options=options)`
   in both `starter_script.py` and `script.py` file. Mention your path instead of `/home/kanish/Documents/chromedriver/chromedriver`.

    **`starter_script.py`**
    ![img](img2.png)

    **`script.py`**
    ![img](img1.png)

3. Now you have to run the script `starter_script.py` given above. Run it using the command (in your terminal):

```bash
python3 starter_script.py
```

Then a webpage of codeforces will open. Please login and do tick the checkbox **remember me for month** given there, so that you do not have to login everytime you run the script.
![img](img.png)

The script for submission will work only if you are already logged in.

---

## Usage

Open the code and you will see language variable in it and there are all options for language below it itself in the code. Please copy the one you want to select and paste in the language variable where there is **language = "GNU G++17 7.3.0"**
eg. If you want to select python language then it should be like **language = "Python 3.7.2"**.
**By default I have it is already selected as C++ so incase you want to submit in C++ no need to change it**

Now simply run the script by command:-

```bash
python3 script.py
```

It will ask you for problem code. Example: if problem is 1167G, type `1167G`.

Then you will be asked relative path of your code from current directory. Example: If your code is in the same directory from where you are running this script then simply input code no eg.1167G.cpp

**It is preferrable to keep script in folder where your code is so that you only have to write code name as relative path**

In this script I have mentioned link for problems opened through problemset i.e having link like `https://codeforces.com/problemset/problem/1167/G`, If you want it to submit for other links like in contest then you can change the link in code in line 'driver.get('write you link here for the problem')'

And now simply press enter and see the results :satisfied:.

---

## Contribute

Please feel free to open a PR or submit an issue with your feedback!
