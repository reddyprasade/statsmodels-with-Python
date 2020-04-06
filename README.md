![](https://www.statsmodels.org/stable/_images/statsmodels-logo-v2-horizontal.svg)
# Statsmodels-with-Python
statsmodels is a Python module that provides classes and functions for the estimation of many different statistical models, as well as for conducting statistical tests, and statistical data exploration. An extensive list of result statistics are available for each estimator. The results are tested against existing statistical packages to ensure that they are correct. 
<div class="md-content">
          <article class="md-content__inner md-typeset" role="main">
            
  
<span id="install"></span><h1 id="install--page-root">Installing statsmodels<a class="headerlink" href="#install--page-root" title="Permalink to this headline">¶</a></h1>
<p>The easiest way to install statsmodels is to install it as part of the <a class="reference external" href="https://docs.continuum.io/anaconda/">Anaconda</a>
distribution, a cross-platform distribution for data analysis and scientific
computing. This is the recommended installation method for most users.</p>
<p>Instructions for installing from PyPI, source or a development version are also provided.</p>

<h2 id="python-support">Python Support<a class="headerlink" href="#python-support" title="Permalink to this headline">¶</a></h2>
<p>statsmodels supports Python 3.5, 3.6 and 3.7.</p>


<h2 id="id1">Anaconda<a class="headerlink" href="#id1" title="Permalink to this headline">¶</a></h2>
<p>statsmodels is available through conda provided by
<a class="reference external" href="https://www.continuum.io/downloads">Anaconda</a>. The latest release can
be installed using:</p>
<div class="highlight-bash notranslate"><div class="highlight"><pre><span></span>conda install -c conda-forge statsmodels
</pre></div>
</div>


<h2 id="pypi-pip">PyPI (pip)<a class="headerlink" href="#pypi-pip" title="Permalink to this headline">¶</a></h2>
<p>To obtain the latest released version of statsmodels using pip:</p>
<div class="highlight-bash notranslate"><div class="highlight"><pre><span></span>pip install statsmodels
</pre></div>
</div>
<p>Follow <a class="reference external" href="https://pypi.org/project/statsmodels/">this link to our PyPI page</a> to directly
download wheels or source.</p>
<p>For Windows users, unofficial recent binaries (wheels) are occasionally
available <a class="reference external" href="https://www.lfd.uci.edu/~gohlke/pythonlibs/#statsmodels">here</a>.</p>


<h2 id="obtaining-the-source">Obtaining the Source<a class="headerlink" href="#obtaining-the-source" title="Permalink to this headline">¶</a></h2>
<p>We do not release very often but the master branch of our source code is
usually fine for everyday use. You can get the latest source from our
<a class="reference external" href="https://github.com/statsmodels/statsmodels">github repository</a>. Or if you
have git installed:</p>
<div class="highlight-bash notranslate"><div class="highlight"><pre><span></span>git clone git://github.com/statsmodels/statsmodels.git
</pre></div>
</div>
<p>If you want to keep up to date with the source on github just periodically do:</p>
<div class="highlight-bash notranslate"><div class="highlight"><pre><span></span>git pull
</pre></div>
</div>
<p>in the statsmodels directory.</p>


<h2 id="installation-from-source">Installation from Source<a class="headerlink" href="#installation-from-source" title="Permalink to this headline">¶</a></h2>
<p>You will need a C compiler installed to build statsmodels. If you are building
from the github source and not a source release, then you will also need
Cython. You can follow the instructions below to get a C compiler setup for
Windows.</p>
<p>If your system is already set up with pip, a compiler, and git, you can try:</p>
<div class="highlight-bash notranslate"><div class="highlight"><pre><span></span>pip install git+https://github.com/statsmodels/statsmodels
</pre></div>
</div>
<p>If you do not have pip installed or want to do the installation more manually,
you can also type:</p>
<div class="highlight-bash notranslate"><div class="highlight"><pre><span></span>python setup.py install
</pre></div>
</div>
<p>Or even more manually</p>
<div class="highlight-bash notranslate"><div class="highlight"><pre><span></span>python setup.py build
python setup.py install
</pre></div>
</div>
<p>statsmodels can also be installed in <cite>develop</cite> mode which installs statsmodels
into the current python environment in-place. The advantage of this is that
edited modules will immediately be re-interpreted when the python interpreter
restarts without having to re-install statsmodels.</p>
<div class="highlight-bash notranslate"><div class="highlight"><pre><span></span>python setup.py develop
</pre></div>
</div>

<h3 id="compilers">Compilers<a class="headerlink" href="#compilers" title="Permalink to this headline">¶</a></h3>

<h4 id="linux">Linux<a class="headerlink" href="#linux" title="Permalink to this headline">¶</a></h4>
<p>If you are using Linux, we assume that you are savvy enough to install <cite>gcc</cite> on
your own. More than likely, it is already installed.</p>


<h4 id="windows">Windows<a class="headerlink" href="#windows" title="Permalink to this headline">¶</a></h4>
<p>It is strongly recommended to use 64-bit Python if possible.</p>
<p>Getting the right compiler is especially confusing for Windows users. Over time,
Python has been built using a variety of different Windows C compilers.
<a class="reference external" href="https://wiki.python.org/moin/WindowsCompilers">This guide</a> should help
clarify which version of Python uses which compiler by default.</p>


<h4 id="mac">Mac<a class="headerlink" href="#mac" title="Permalink to this headline">¶</a></h4>
<p>Installing statsmodels on MacOS requires installing <cite>gcc</cite> which provides
a suitable C compiler. We recommend installing Xcode and the Command Line
Tools.</p>




<h2 id="dependencies">Dependencies<a class="headerlink" href="#dependencies" title="Permalink to this headline">¶</a></h2>
<p>The current minimum dependencies are:</p>
<ul class="simple">
<li><p><a class="reference external" href="https://www.python.org">Python</a> &gt;= 3.5</p></li>
<li><p><a class="reference external" href="https://www.scipy.org/">NumPy</a> &gt;= 1.14</p></li>
<li><p><a class="reference external" href="https://www.scipy.org/">SciPy</a> &gt;= 1.0</p></li>
<li><p><a class="reference external" href="https://pandas.pydata.org/">Pandas</a> &gt;= 0.21</p></li>
<li><p><a class="reference external" href="https://patsy.readthedocs.io/en/latest/">Patsy</a> &gt;= 0.5.1</p></li>
</ul>
<p>Cython is required to build from a git checkout but not to run or install from PyPI:</p>
<ul class="simple">
<li><p><a class="reference external" href="https://cython.org/">Cython</a> &gt;= 0.29 is required to build the code from
github but not from a source distribution.</p></li>
</ul>
<p>Given the long release cycle, statsmodels follows a loose time-based policy for
dependencies: minimal dependencies are lagged about one and a half to two
years. Our next planned update of minimum versions is expected in the first
half of 2020.</p>


<h2 id="optional-dependencies">Optional Dependencies<a class="headerlink" href="#optional-dependencies" title="Permalink to this headline">¶</a></h2>
<ul class="simple">
<li><p><a class="reference external" href="https://cvxopt.org/">cvxopt</a> is required for regularized fitting of
some models.</p></li>
<li><p><a class="reference external" href="https://matplotlib.org/">Matplotlib</a> &gt;= 2.2 is needed for plotting
functions and running many of the examples.</p></li>
<li><p>If installed, <a class="reference external" href="https://www.census.gov/srd/www/x13as/">X-12-ARIMA</a> or
<a class="reference external" href="https://www.census.gov/srd/www/x13as/">X-13ARIMA-SEATS</a> can be used
for time-series analysis.</p></li>
<li><p><a class="reference external" href="https://docs.pytest.org/en/latest/">pytest</a> is required to run
the test suite.</p></li>
<li><p><a class="reference external" href="https://ipython.org">IPython</a> &gt;= 5.0 is required to build the
docs locally or to use the notebooks.</p></li>
<li><p><a class="reference external" href="http://pythonhosted.org/joblib/">joblib</a> &gt;= 0.9 can be used to accelerate distributed
estimation for certain models.</p></li>
<li><p><a class="reference external" href="https://jupyter.org/">jupyter</a> is needed to run the notebooks.</p></li>
</ul>
