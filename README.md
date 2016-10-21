## We use Gulp (http://gulpjs.com/) to manage our build process.

### To use

#### Install dependencies

Node (4.2.2 or greater is required):

```
node -v
```

If your node is out of date, install the latest from:
http://nodejs.org/

After node is setup, install the other dependencies:

```
# Install Gulp-Cli
npm install gulp-cli -g

# Install all the dependencies for this project.
npm install

# Make sure you have the latest of all the CreateJS libraries.
```

#### Setup

You'll need to change the default settings to suit your work environment.
We have 2 config files:

* `config.json` - Is meant to be in git and pushed to all developers.
* `config.local.json` - Is added to `.gitignore` and only for your local setup (any settings in here will override those in `config.json`)

Please adjust these settings to match your environment. All paths can either be relative from this folder, or absolute paths.

* `site_path`
* `easel_path`
* `preload_path`
* `sound_path`
* `tween_path`

#### Building
To export a release build for this library run:

```
npm run build
```

This command will bundle all libs together.

To build the NEXT version run:

```
npm run build:next
```

Does the exact same process as above but uses NEXT as the version.

#### Main commands
* `npm run build` - Builds all the projects and creates combined / minified files
* `npm run build:next` - Same as build, but uses the NEXT version.
* `npm run cdn` - Builds a new CDN index page and copies all required script files to build.
