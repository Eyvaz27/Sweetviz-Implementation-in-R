#' Building a function in order to replicate 'show_html' function in sweetviz
#' The analyze() function can take multiple other arguments
#' show_html(...) will create and save an HTML report at the given file path
#' @param layout Either 'widescreen' or 'vertical'.
#' The widescreen layout displays details on the right side of the screen,
#' as the mouse goes over each feature.
#' @param scale Use a floating-point number (scale= 0.8 or None) to scale
#' the entire report. This is very useful to fit reports to any output.
#' @param open_browser Enables the automatic opening of a web browser to show
#' the report. Since under some circumstances this is not desired (or causes
#' issues with some IDE's), you can disable it here.
#' @return Nothing is returned, instead, descriptive ".html" file is created
#' in the current working directory
#' @author Eyvaz Najafli
#' @details Sweetviz currently supports Python 3.6+ and Pandas 0.25.3+.
#' Reports are output using the base "os" module, so custom environments
#' such as Google Colab which require custom file operations are not yet supported,
#' although I am looking into a solution.
#' @seealso \href{https://pypi.org/project/sweetviz/}{Sweetviz}
#' @export

generate.report <- function(data){
  sv <- reticulate:::import('sweetviz')
  report <- sv$analyze(data)
  report$show_html('Analysis.html')
}


