# StockPricePrediction
Use RNN to predict stock prices

Make use of a recurrent neural network and multiple indicators to train different models that can predict open stock prices (here: Google).
* Lowest Mean Squared Error (mse) can be achieved with one indicator (open price), where the model is trained with data of a time from 2004 to 2016.
* Highest accuracy can be achieved with one indicator (open price), where the model is trained with data of a time from 2012 to 2016.
* Best overall performance (low mse and high accuracy) is realized by a RNN, that is trained with two indicators (open price & volume) with data of a time from 2012 to 2016.

Inspired by udemy course “Deep Learning A-Z”

| notebook                                           | regressor (h5)                         | training time frame | indicators                          | mse   | direction accuracy |
|----------------------------------------------------|----------------------------------------|---------------------|-------------------------------------|-------|--------------------|
| 210430_BaseModel_OneInd_2012-2016                  | reg_google_2012-2016.h5                | 2012-2016           | open price                          | 0.015 | 0.75               |
| 210429_BaseModel_OneInd_2004_2016                  | reg_google_2004-2016.h5                | 2004-2016           | open price                          | 0.014 | 0.6                |
| 210506_BaseModel_TwoInd_OpenHigh_2012-2016         | reg_google_ind2_open_high_2012-2016.h5 | 2012-2016           | open price & close price            | 0.018 | 0.7                |
| 210512_BaseModel_TwoInd_OpenClose_2012-2016        | reg_google_ind2_open_close_2012-2016   | 2012-2016           | open price & high price             | 0.022 | 0.7                |
| 210513_BaseModel_TwoInd_OpenClose_transp_2012_2016 | reg_ind2_open_close_transp_2012-2016   | 2012-2016           | open price & transposed close price | 0.022 | 0.65               |
| 210520_BaseModel_TwoInd_OpenVolume_2012_2016       | reg_ind2_open_volume_2012-2016         | 2012-2016           | open price & volume                 | 0.014 | 0.7                |
