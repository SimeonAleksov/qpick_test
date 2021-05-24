# Django polls tutorial

## Setup

The first thing to do is to clone the repository:

```sh
$ git clone https://github.com/SimeonAleksov/qpick_test
$ cd qpick_test
```

Create a virtual environment to install dependencies in and activate it:

```sh
$ python3 -m venv venv
$ source venv/bin/activate
```

Then install the dependencies:

```sh
(venv)$ pip install -r requirements.txt
```

Once `pip` has finished downloading the dependencies, run the migrations:
```sh
(venv)$ python manage.py migrate
```

I have also included example fixtures, so just load them:
```sh
(venv)$ python manage.py loaddata fixtures/question.json --app polls.question
(venv)$ python manage.py loaddata fixtures/choice.json --app polls.choice
```
And navigate to `http://127.0.0.1:8000/polls/`.

## Note

As this is just a sample project, I haven't used any environemnt variables, nor split the settings, in a real-life project, [like this one for example](https://github.com/SimeonAleksov/shigoto_q) the structure wouldn't look exactly like this.
