Baseball Analysis

This project is best for seaborn library reference. Baseball knowledge makes it exciting but not required perse.

Uncommon methods used:

pandas

1. pd.set_option('display.max_columns', None)

- Displays all columns without dotting out some.
- Try pd.set_option("display.max_rows", 101)

2. df.apply(function)

- Two ways of using this is discussed. One applying to pd.Series directly.

- Other applying on every row, and using `row.column` inside the function with axis=1.

Note - Try using df.assign if new column is only for specific analysis and no further usage(ensures no inplace change of df)

seaborn

1. sns.regplot(x=columnx, y=columny, data=df, fit_reg=False, color=color,  ax=axes[index]).set_title(Title) 

- Just turning off fit_reg, a statistical plot is used to beautifully depict relation between two variables.

- Chaining of set_title method is notable.

2. sns.kdeplot(df.columnx, df.columny, cmap="Blues", shade=True, shade_lowest=False, ax=axes[index]).set_title(Title)

- kernal density plot is little used often, but truly brings out another dimension in bivariate analysis.

Tip for sns: Passing `rug=True` draws a small vertical tick at each observation, usable in sns.distplot(), `kde=True` gives kernel density estimate plotting the shape of the distribution.

3. sns.boxplot(df=df, x= columnx, y=columny).set_title(Title)

- Useful when x has categories within, and y has corresponding values for further analysis.

matplotlib

1. plt.hist2d(df[columnx], df[columny], bins = n, cmap='color')

- Beautiful implementation of hist2d, useful in glossing two columns with same range of values, with similar meanings.

2. fig1, axs1 = plt.subplots(ncols=2, sharex=True, sharey=True)

- Sharing x and y is useful in comparing similar information
