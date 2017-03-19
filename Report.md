Suhas Maringanti

CSC-338 Assignment 1 Report

Number of cores on the test machine(Windows): 4

1.  Results for risk\_serial.py:

  Simulations   Time(s)
  ------------- ---------
  25            1.89
  50            3.85
  75            5.76
  100           7.42

1.  Results for risk\_thr.py:

  Simulations   Time(s)
  ------------- ---------
  25            1.82
  50            3.75
  75            5.67
  100           7.44

1.  Results for risk\_mp.py:

  Simulations   Time(s)
  ------------- ---------
  25            0.60
  50            1.06
  75            1.57
  100           2.20

Because of python’s global interpreter lock, threads cannot run
concurrently. Since there is not much overhead in I/O operations in the
serial program, risk\_thr.py runs as fast as risk\_serial.py. However,
risk\_mp.py uses multiple processes that run in parallel and hence
outperforms risk\_serial.py and risk\_thr.py.
