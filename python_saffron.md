### Python Tips  
  
General  
* List of characters of a string:  
	list('banana') returns a list of each characters.  
* Get values from a string with list comprehension:  
	(a, b, c) = [ x for x in STRING.split() ]  
*  reversing a list's items:  
	LIST.reverse()  
* with statement mostly for opening files and close automatically:  
	with open(“PATH”, “MODE”) as mfile:  
		lines = mfile.readlines()  
* enumerate returns tuple of (index, value):  
	for i, num in enumerate(np.random.randint(0, max, size=count))  
* Pretty Printer, to print all abstracts in Python:   
	pprint()  
* Set, sorted and duplicate-free:  
	{1, 2, 3, 3, 9, 0} -> {0, 1, 2 ,3, 9}  
* Disctionary:  
	{1:11, 2:22, 3:33}  
  
TensorFlow  
* TF and Theano both expect a 4-dimnesional tensor as input to convolutional layers.   
* tf.backend.image_data_format() == 'channels-last' (TF default): (samples, rows, cols, channels), == 'channel-first':  (samples, channels, rows, cols)  
* model = keras.Sequential() aliases keras.models.Sequential()  
  
Pandas  
* Convert data frame to numpy to select rows and columns easier:  
	x_train = train.values[:, 1:], y_train = train.values[:, 0]  
* Counting number of items fall in each label (COLUMN) classes:  
	df.groupby('COLUMN').count()  
* Access to rows:  
	df.iloc[INDEX]  or  df.loc['ROW_LABEL']  
* Access to columns:  
	df['COL_LABEL']  
* Conditional selection:  
	df.loc[df['COL_LABEL'] == VALUE]  
* Sum of a column or a row:  
	df['COL_LABEL'].sum()  or  df.iloc[INDEX].sum()  
  
  
Matplotlib  
* Math formula in text (labels, title, etc.) using r controller in body text:  
	plt.xlabel(r'$\alpha * \beta$)  
* Matplotlib colormaps:  
	https://matplotlib.org/tutorials/colors/colormaps.html  
* New plot. Necessary before each plots:  
	plt.figure()  
* Subplot. Several plots in one plot (iteratable over INDEX in a loop):  
	plt.subplot(NROWS, NCOLS, INDEX)  
* Plot image size. Dimension are multiplied by 100 for real pixel size (e.g. (8, 6) -> (800, 600)):  
	plt.figure(figsize=(W, H))  
* Color bar:  
	plt.colorbar()  
* No ticks:  
	plt.xticks([])  
	plt.yticks([])  
  
Anaconda & PIP  
* Package installation: make sure that you're working in the desired env:   
	$ source activate <env>  
* Update all Anaconda packages:  
	$ conda update --all  
* Update all PIP packages:  
	-e:  skip editable in grep (can replace grep+cut with sed or awk or perl)  
	-n1: prevents stopping everything if updating one package fails in xargs  
	$ pip list --outdated --format=freeze | grep -v '^\-e' | cut -d = -f 1  | xargs -n1 pip install -U  
  
Jupyter Notebook  
* before starting a notebook, make sure that right conda env is activated!  
