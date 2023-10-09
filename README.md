# Python-ile--check-df--fonksiyonu
# Veri biliminde bir dataframe'e hızlı bir şekilde göz atarak veri hakkında ön bilgiye sahip olmamızı sağlayan bir fonksiyon.
# import:
    import numpy as np
    import pandas as pd
    import seaborn as sns
    import matplotlib.pyplot as plt
    pd.set_option('display.width', 500)
    pd.set_option('display.max.columns', None)
    df = sns.load_dataset("titanic")

# def check_df(dataframe, hd=5):
    print("######################## Shape ########################")
    print(dataframe.shape)
    print("######################## Type ########################")
    print(dataframe.dtypes)
    print("######################## Head ########################")
    print(dataframe.head(hd))
    print("######################## Tail ########################")
    print(dataframe.tail(hd))
    print("######################## NA ########################")
    print(dataframe.isnull().sum())
    print("######################## Quantiles ########################")
    print(dataframe.describe().T)

check_df(df)

