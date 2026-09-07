from sklearn.compose import ColumnTransformer

transformer = ColumnTransfromer(transformers=[
('tnf1' ,  transformer_function_1,  ['columns_ name']),
('tnf2' , tansformer_funtion_2,['columns_name'])
]
remainder = 'left column'

)


1. ColumnTransfromer is a Class.
2. transformers and remainder is a arrugument that we need to give it.
3.  **transformers**  : list of tuples

List of (name, transformer, columns) tuples specifying the transformer objects to be applied to subsets of the data.

name : str -> name of the transformer that we gonna applied on column
transformer : transformer_function that we need to applied on columns
columns_name : list of columns name that we need to transforms



transformer{‘drop’, ‘passthrough’} or estimator

Estimator must support [fit](https://scikit-learn.org/stable/glossary.html#term-fit) and [transform](https://scikit-learn.org/stable/glossary.html#term-transform). Special-cased strings ‘drop’ and ‘passthrough’ are accepted as well, to indicate to drop the columns or to pass them through untransformed, respectively.

columns : str, array-like of str, int, array-like of int, array-like of bool, slice or callable

Indexes the data on its second axis. Integers are interpreted as positional columns, while strings can reference DataFrame columns by name.