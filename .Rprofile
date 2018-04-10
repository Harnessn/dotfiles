options(
    repos = c(CRAN = "https://cran.rstudio.com"),
    # browserNLdisabled = TRUE,
    # deparse.max.lines = 2,
    max.print = 200,
    rtichoke.color_scheme = "native",
    rtichoke.history_search_no_duplicates = TRUE,
    rtichoke.auto_match = TRUE
    # rice.insert_new_line = FALSE
    # rice.auto_indentation = FALSE
    # rice.complete_while_typing = FALSE
)

utils::rc.settings(ipck = TRUE)


# mac only
if (Sys.info()["sysname"] == "Darwin"){
    if (interactive()) {
        Sys.setenv(TZ = "America/New_York")
        try(suppressMessages(library(prettycode)), silent = TRUE)
        options(
            device = "quartz",
            help_type = "html"
        )
        setHook(packageEvent("grDevices", "onLoad"),
                function(...) grDevices::quartz.options(
                    width = 5,
                    height = 5,
                    pointsize = 8
                ))
    } else {
        options(
            repr.plot.width = 5,
            repr.plot.height = 5,
            repr.plot.res = 100,
            jupyter.plot_mimetypes = "image/png"
        )
    }
}
