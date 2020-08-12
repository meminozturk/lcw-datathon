# Winning Solution to LC Waikiki Datathon 2019

We're proud of successfully winning the first place in LC Waikiki Datathon 2019 in Istanbul between March 8-10 2019. LC Waikiki is the largest Turkish retailer founded in France in 1988. Today, LC Waikiki trades in 1018 stores in 47 countries.

The main case of the datathon was simply sales forecasting by analyzing the past period data, finding the factors affecting the sales and making a sales forecast on the basis of category (class) in the day-store-product hierarchy for future periods.

We developed a predictive model on Python scoring RMSE of 4.26, which brought us the winning position. It was mainly a Lightgbm model with some special tricks;

* We tested all hypothesis over expanding window validation scheme to represent the real life.

* We fed our daily forecast model with the weekly results we obtained by reducing the data to a weekly level and building models with many more variables before daily predictions.

* Instead of representing special days like Mother's Day with binary variables, we calculated the number of days left for these special days. Because we mostly prepare for our special days just before that day.

* We included daily temperature differences in the model to take into account sudden weather changes.

* We used categorical values such as StoreID and ProductID by converting them to numerical values with the help of Target Encoding, Dummification and Label Encoding.

I can't share the code and the data because of confidentiality issues since the data given to us was real sales values of LC Waikiki between 2015-2018. You can see more details about the datathon over the project url which refers the official blog post by LC Waikiki.

Thanks,

Emin
