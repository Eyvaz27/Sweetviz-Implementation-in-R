#' Building a function in order to replicate 'linspace' function in numpy
#' Return evenly spaced numbers over a specified interval.
#' Returns num evenly spaced samples, calculated over the interval [start, stop].
#' The endpoint of the interval can optionally be excluded.
#' @param start The starting value of the sequence.
#' @param stop The end value of the sequence, unless endpoint is set to False.
#' @param num Number of samples to generate. Default is 50. Must be non-negative.
#' @param endpoint If True, stop is the last sample. Otherwise, it is not included. Default is True.
#' @return samples There are num equally spaced samples in the closed interval
#' @return step Only returned if retstep is True
#' @author Eyvaz Najafli
#' @details
#' Changed in version 1.16.0:
#' Non-scalar start and stop are now supported.
#' Changed in version 1.20.0:
#' Values are rounded towards -inf instead of 0
#' when an integer dtype is specified.
#' The old behavior can still be obtained with
#' np.linspace(start, stop, num).astype(int)
#' @seealso \href{https://numpy.org/doc/stable/reference/generated/numpy.linspace.html}{Linspace}
#' @export

linspace <- function(start, stop, num=50L, endpoint=T, retstep=F, dtype=NULL, axis=0L){
  np <- reticulate:::import('numpy')
  if(typeof(start)!='integer' | typeof(stop)!='integer' | typeof(num)!='integer'){
    stop("Type Mismatch occured in input")}
  else{
    if(is.null(dtype)){
      return(np$linspace(start, stop, num, endpoint, retstep, axis=axis))
    }
    else{
      return(np$linspace(start, stop, num, endpoint, retstep, reticulate::r_to_py(dtype), axis))
    }
  }
}

