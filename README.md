** Hello **

**_ Dependencies _**
We will be using air for live reloading and fiber for api use!

-   go get github.com/gofiber/fiber/v2
-   go get github.com/air-verse/air@latest

````toml`

# basic air toml set up for live reloading

##########################################
root = "." # The root directory of the project
tmp_dir = "tmp" # The temporary directory where air will store its temporary files

[build] # The build configuration
bin = "main" # The name of the binary file to be generated after building the project
cmd = "go build -o {{.Output}} {{.Input}}" # The command to build the project
exclude = ["tmp/*", "client/*"] # Specifies the directories to be excluded from monitoring for changes
include = ["**/*.go"] # Specifies the file patterns to be included for monitoring.
ignore = ["tmp/*"] # Specifies the files or directories to be ignored when triggering a build.

```


```
