# 11ty Blog from Scratch

---

## Step 1 (Getting Started)

---

Create a new directory and change to that directory:

```
~ $ mkdir 11ty
~ $ cd 11ty
```

Initialize this directory as a git repository:

```
~/11ty $ git init
```

Create `.gitignore` file:

```
touch .gitignore
```

Add following to `.gitignore`:

```
_site/
node_modules/
.nyc_output/
coverage/
package-lock.json
```

Create `.editorconfig` file:

```
~/11ty $ touch .editorconfig
```

Add following to `.editorconfig` file:

```
root = true

[*]
indent_style = space
indent_size = 2
end_of_line = lf
insert_final_newline = false
trim_trailing_whitespace = true
charset = utf-8

[*.js]
insert_final_newline = true
```

Create `README.md` file:

```
~/11ty $ touch README.md
```

Create a `package.json` file:

```
~/11ty $ npm init -y
```

Install `eleventy` locally into `package.json`:

```
~/11ty $ npm install --save-dev @11ty/eleventy
```

Add `start` script to `package.json` that uses `npx` to run our local project version's version of `eleventy` OR run the following command:

```
~/11ty $ npx @11ty/eleventy
Processed 0 files in 0.03 seconds (v0.9.0)
```

is same as:

```
~/11ty $ npx @11ty/eleventy --input=. --output=_site
```

This command searches the current directory, outputs to `./_site`.

Eleventy didn't process any files because we have an empty folder with no templates inside.

## 11ty Commands to Know

---

```bash
# Searches the current directory, outputs to ./_site
~/11ty $ npx @11ty/eleventy
```

`--formats`

```bash
# Use only a sebset of template types
~/11ty $ npx @11ty/eleventy --formats=md, html, ejs
```

`--help`

```bash
# Find out the list of commands
~/11ty $ npx @11ty/eleventy --help
```

`--serve`

```bash
# Boot up a Browsersync web server to apply changes and refresh automatically. This will also --watch for you
~/11ty $ npx @11ty/eleventy --serve
```

`--config` to change the config file name:

```bash
# Override th default eleventy project config filename (.eleventy.js)
~/11ty $ npx @11ty/eleventy --config=myeleventyconfig.js
```
