# Double quoting file patterns

## Testing folder structure

8 files in total.

```
files/
├── components
│   ├── footer.css
│   ├── header.css
│   ├── navigation.css
│   └── user
│       └── avatar.css
├── main.css
└── pages
    ├── detail.css
    ├── index.css
    └── listings.css

3 directories, 8 files
```

## Testing commands

I want to match all 8 css files in `files` folder.

Try the following commands, they give you wrong matches:

1. `$ npm run cli-in-root`.
1. `$ npm run cli-in-root-double-quote`.
1. `$ npm run cli-in-npm`.
1. `$ npm run cli-in-npm-double-quote`.

Only calling script without npm gives the correct match:

1. `$ ./cli.js files/**/*.css`.
1. `$ ./node_modules/.bin/cli ./files/**/*.css`.

**WTF?!**
