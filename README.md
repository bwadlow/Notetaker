Notetaker
======================

## Setup

The codebase is split up into a Rails API backend and a React frontend. Everything is contained in this single repository. Rails code is located inside of the `backend` folder and React code is located inside of the `frontend` folder.

### Frontend

```sh
# from within this directory:
npm install
PORT=4000 npm start
```

This React app will be running on `http://localhost:4000`.

### Backend

```sh
# from within this directory:
bundle install
rails db:create db:migrate db:seed
rails s
```
Rails backend API will be running on `http://localhost:3000`.

### Video Demo

https://youtu.be/I12vkBWEl4c
