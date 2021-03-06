## PyFladesk
Create desktop application by using Flask and QtWebKit 

## Idea

Rather than open Flask app in user browser, create a QWebview and then run Flask app on it.

By default, every internal link is open inside the app and every external link is open in the default browser.

## Dependencies

- Python3
- Flask
- PyQt

Note: Some releases require Conda to properly create a virtual environment

## Versions

There are 3 available versions:

- [PyQt4](https://github.com/smoqadam/PyFladesk/releases/tag/0.1)
- [PyQt5.6](https://github.com/smoqadam/PyFladesk/releases/tag/0.2)
- [PyQt5.10](https://github.com/smoqadam/PyFladesk/releases/tag/1.0)

Note: Both PyQt4 and PyQt5.6 are only made available for compatibility reasons, there is no intention to keep them updated unless requested

## Usage

### New Flask App

1. Download the [lastest release](https://github.com/smoqadam/PyFladesk/releases) and extract it
2. Add your routes in `routes.py`

Example:

```python
from flask import render_template
from app import app

@app.route('/')
def index():
    return render_template('index.html')

@app.route('/page2')
def page2():
    return render_template('page2.html')
```

3. Run `app.py`

Linux:
`> python3 app.py`

Windows:
`> python app.py`

### Existing Flask App

1. Check dependences of your project and choose a branch accordingly
2. Download the gui.py 
3. Replace `app.run` with `init_gui(app)`

#### Sample RSS Reader app

I wrote a sample Rss reader app by PyFladesk. you can find it [here](https://github.com/smoqadam/PyFladesk-rss-reader).

## Contributing

FEEL FREE TO TELL ME IF YOU SEE ANY MISTAKE OR NOTABLE THINGS BY OPENING A NEW ISSUE OR SENDING A PULL REQUEST

## TODOs:

- Create a standalone executable file (pyinstaller, cx_freeze, etc)
- Add different backends (wxPython, TKinter, etc)
- Test performance of HTML5 and CSS3
- Add Directory structure for large projects (Flask Patterns)
- Test other micro web frameworks (Bottle, etc)

## Thanks
Thanks to [Mathias Ettinger](http://codereview.stackexchange.com/users/84718/mathias-ettinger) for his [review](http://codereview.stackexchange.com/questions/114221/python-gui-by-qtwebkit-and-flask/114307#114307)
