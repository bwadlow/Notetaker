README: React Notetaker
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

#### User ID

The seed file should create one user for you, so your default `USER_ID` should be `1`. If that doesn't work, debug it with the `/api/v1/users` route as shown below.

#### Routes

| Method | Route               | Headers                                                              | Body                 |
| ------ | ------------------- |:--------------------------------------------------------------------:|:--------------------:|
| GET    | `/api/v1/users`     |                                                                      |                      |
| GET    | `/api/v1/notes`     |                                                                      |                      |
| POST   | `/api/v1/notes`     | `'Content-Type': 'application/json'`<br/>`'Accept': 'application/json'` | title, body, user_id |
| PATCH  | `/api/v1/notes/:id` | `'Content-Type': 'application/json'`<br/>`'Accept': 'application/json'` | title, body, user_id |



![result](react-evernote-display.gif)

**Editing Notes**

- [ ] When displaying a note in the right panel, show an `Edit` button.
- [ ] Clicking the `Edit` button will allow the user to edit the title and body in the right panel.
- [ ] When in edit mode, also show a `Save` button which saves the note via a `PATCH` request.
- [ ] When in edit mode, also show a `Cancel` button which discards any changes and reverts back to displaying the note.
- [ ] Clicking a different note while in edit mode should discard your changes and display the new note instead.

![result](react-evernote-edit.gif)

**Creating Notes**

- [ ] At the bottom of your left sidebar, show a `New` button.
- [ ] Clicking `New` will create a new note via `POST` request with some default title and body.
- [ ] This new note should appear in the sidebar.

![result](react-evernote-create.gif)

**Filtering Notes**

- [ ] Implement the filter to search through your notes list by title.

![result](react-evernote-filter.gif)
