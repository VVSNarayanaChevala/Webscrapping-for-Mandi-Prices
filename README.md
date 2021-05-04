# Webscrapping-for-Mandi-Prices
Scrapping data from public domains and sites

```python
from autoscraper import AutoScraper

url = 'http://agmarknet.gov.in/SearchCmmMkt.aspx?Tx_Commodity=3&Tx_State=OR&Tx_District=0&Tx_Market=0&DateFrom=01-May-2021&DateTo=04-May-2021&Fr_Date=01-May-2021&To_Date=04-May-2021&Tx_Trend=0&Tx_CommodityHead=Rice&Tx_StateHead=Odisha'

# We can add one or multiple candidates here.
# You can also put urls here to retrieve urls.
wanted_list = ["Keonjhar", "Keonjhar","Rice", "Other", "2500", "2600", "2600", "02 May 2021"]

scraper = AutoScraper()
result = scraper.build(url, wanted_list)
print(result)
```

    ['Keonjhar', 'Keonjhar(Dhekikote)', 'Saharpada', 'Both', 'Castor Oil', 'West Bengal', 'Sundergarh', 'Balekai', 'Maharashtra', 'Bhawanipatna', 'Rice', '2012', 'Z[State Total]', 'Other', '2500', '2600', '02 May 2021', '01 May 2021']



```python
scraper.get_result_similar(url, grouped=True)
```




    {'rule_j2n8': ['Keonjhar',
      'Keonjhar',
      'Keonjhar',
      'Keonjhar',
      'Keonjhar',
      'Keonjhar'],
     'rule_k5c4': ['Keonjhar',
      'Keonjhar',
      'Keonjhar',
      'Keonjhar',
      'Keonjhar',
      'Keonjhar'],
     'rule_i2b0': ['Keonjhar',
      'Keonjhar',
      'Keonjhar',
      'Keonjhar',
      'Keonjhar',
      'Keonjhar'],
     'rule_rwz2': ['Keonjhar',
      'Keonjhar',
      'Keonjhar',
      'Keonjhar',
      'Keonjhar',
      'Keonjhar'],
     'rule_n34t': ['Keonjhar',
      'Keonjhar',
      'Keonjhar(Dhekikote)',
      'Keonjhar(Dhekikote)',
      'Saharpada',
      'Saharpada'],
     'rule_jcsy': ['Keonjhar',
      'Keonjhar',
      'Keonjhar',
      'Keonjhar',
      'Keonjhar',
      'Keonjhar'],
     'rule_d39d': ['Keonjhar',
      'Keonjhar',
      'Keonjhar(Dhekikote)',
      'Keonjhar(Dhekikote)',
      'Saharpada',
      'Saharpada'],
     'rule_vwzn': ['Keonjhar',
      'Keonjhar',
      'Keonjhar',
      'Keonjhar',
      'Keonjhar',
      'Keonjhar'],
     'rule_3te3': ['Both', 'Castor Oil', 'West Bengal', 'Sundergarh', 'Keonjhar'],
     'rule_ngqs': ['Both', 'Balekai', 'Maharashtra', 'Keonjhar', 'Bhawanipatna'],
     'rule_cxgb': ['Rice', 'Rice', 'Rice', 'Rice', 'Rice', 'Rice'],
     'rule_snh6': ['Rice', 'Rice', 'Rice', 'Rice', 'Rice', 'Rice'],
     'rule_kx4c': ['Rice', 'Rice', 'Rice', 'Rice', 'Rice', 'Rice'],
     'rule_02tu': ['Rice', 'Rice', 'Rice', 'Rice', 'Rice', 'Rice'],
     'rule_inkv': ['Rice', 'Rice', 'Rice', 'Rice', 'Rice', 'Rice'],
     'rule_plnz': ['Rice', 'Rice', 'Rice', 'Rice', 'Rice', 'Rice'],
     'rule_bsp4': ['Rice', '2012', '2012'],
     'rule_m1vu': ['Both', 'Rice', 'West Bengal', 'Sundergarh', 'Z[State Total]'],
     'rule_amxy': ['Other', 'Other', 'Other', 'Other', 'Other', 'Other'],
     'rule_a2h0': ['Other', 'Other', 'Other', 'Other', 'Other', 'Other'],
     'rule_77kf': ['Other', 'Other', 'Other', 'Other', 'Other', 'Other'],
     'rule_c2mn': ['Other', 'Other', 'Other', 'Other', 'Other', 'Other'],
     'rule_t2nl': ['Other', 'Other', 'Other', 'Other', 'Other', 'Other'],
     'rule_75ah': ['Other', 'Other', 'Other', 'Other', 'Other', 'Other'],
     'rule_d2n2': ['2500', '2500', '2500', '2500', '2500', '2500'],
     'rule_onj5': ['2600', '2600', '2600', '2600', '2500', '2600'],
     'rule_n3ml': ['2500', '2500', '2500', '2500', '2500', '2500'],
     'rule_1f0o': ['2500', '2500', '2500', '2500', '2500', '2500'],
     'rule_gqlh': ['2500', '2500', '2500', '2500', '2500', '2500'],
     'rule_pnzm': ['2500', '2500', '2500', '2500', '2500', '2500'],
     'rule_l1qn': ['2500', '2500', '2500', '2500', '2500', '2500'],
     'rule_hchn': ['2600', '2600', '2600', '2600', '2500', '2600'],
     'rule_tm05': ['2600', '2600', '2600', '2600', '2600', '2600'],
     'rule_iggm': ['2600', '2600', '2600', '2600', '2600', '2600'],
     'rule_g5nn': ['2600', '2600', '2600', '2600', '2500', '2600'],
     'rule_mzrl': ['2600', '2600', '2600', '2600', '2600', '2600'],
     'rule_f8wi': ['2600', '2600', '2600', '2600', '2500', '2600'],
     'rule_bz56': ['2600', '2600', '2600', '2600', '2600', '2600'],
     'rule_c2h6': ['2600', '2600', '2600', '2600', '2500', '2600'],
     'rule_6eki': ['2600', '2600', '2600', '2600', '2600', '2600'],
     'rule_utpv': ['2600', '2600', '2600', '2600', '2500', '2600'],
     'rule_4v6q': ['2600', '2600', '2600', '2600', '2600', '2600'],
     'rule_v1wf': ['02 May 2021',
      '01 May 2021',
      '02 May 2021',
      '01 May 2021',
      '02 May 2021',
      '01 May 2021'],
     'rule_t07j': ['02 May 2021',
      '01 May 2021',
      '02 May 2021',
      '01 May 2021',
      '02 May 2021',
      '01 May 2021'],
     'rule_drie': ['02 May 2021',
      '01 May 2021',
      '02 May 2021',
      '01 May 2021',
      '02 May 2021',
      '01 May 2021']}




```python
scraper.get_result_similar(url, grouped=True)
scraper.set_rule_aliases({'rule_j2n8': 'District Name', 
                          'rule_n34t': 'Market Name',
                          'rule_cxgb': 'Commodity',
                          'rule_amxy':'Variety',
                          'rule_d2n2':'Min Price (Rs./Quintal)',
                          'rule_4v6q':'Max Price (Rs./Quintal)',
                          'rule_onj5':'Modal Price (Rs./Quintal)',
                          'rule_v1wf': 'Price Date'
                         })
scraper.keep_rules(['rule_j2n8', 'rule_n34t', 'rule_cxgb', 'rule_amxy', 
                    'rule_d2n2', 'rule_4v6q', 'rule_onj5', 'rule_v1wf'])
scraper.save("OR-Search")
result = scraper.get_result_similar(url, group_by_alias=True)
```


```python
result
```




    {'District Name': ['Keonjhar',
      'Keonjhar',
      'Keonjhar',
      'Keonjhar',
      'Keonjhar',
      'Keonjhar'],
     'Market Name': ['Keonjhar',
      'Keonjhar',
      'Keonjhar(Dhekikote)',
      'Keonjhar(Dhekikote)',
      'Saharpada',
      'Saharpada'],
     'Commodity': ['Rice', 'Rice', 'Rice', 'Rice', 'Rice', 'Rice'],
     'Variety': ['Other', 'Other', 'Other', 'Other', 'Other', 'Other'],
     'Min Price (Rs./Quintal)': ['2500', '2500', '2500', '2500', '2500', '2500'],
     'Modal Price (Rs./Quintal)': ['2600', '2600', '2600', '2600', '2500', '2600'],
     'Max Price (Rs./Quintal)': ['2600', '2600', '2600', '2600', '2600', '2600'],
     'Price Date': ['02 May 2021',
      '01 May 2021',
      '02 May 2021',
      '01 May 2021',
      '02 May 2021',
      '01 May 2021']}




```python
url = 'http://agmarknet.gov.in/SearchCmmMkt.aspx?Tx_Commodity=3&Tx_State=OR&Tx_District=0&Tx_Market=0&DateFrom=01-May-2021&DateTo=04-May-2021&Tx_Trend=0&Tx_CommodityHead=Rice&Tx_StateHead=Odisha'
#url = 'http://agmarknet.gov.in/SearchCmmMkt.aspx?Tx_Commodity=3&Tx_State=OR&Tx_District=0&Tx_Market=0&DateFrom=01-Jan-2021&DateTo=04-May-2021&Fr_Date=01-Jan-2021&To_Date=04-May-2021&Tx_Trend=0&Tx_CommodityHead=Rice&Tx_StateHead=Odisha'
result = scraper.get_result_similar(url, group_by_alias=True)
result
```




    {'District Name': ['Keonjhar',
      'Keonjhar',
      'Keonjhar',
      'Keonjhar',
      'Keonjhar',
      'Keonjhar'],
     'Market Name': ['Keonjhar',
      'Keonjhar',
      'Keonjhar(Dhekikote)',
      'Keonjhar(Dhekikote)',
      'Saharpada',
      'Saharpada'],
     'Commodity': ['Rice', 'Rice', 'Rice', 'Rice', 'Rice', 'Rice'],
     'Variety': ['Other', 'Other', 'Other', 'Other', 'Other', 'Other'],
     'Min Price (Rs./Quintal)': ['2500', '2500', '2500', '2500', '2500', '2500'],
     'Modal Price (Rs./Quintal)': ['2600', '2600', '2600', '2600', '2500', '2600'],
     'Max Price (Rs./Quintal)': ['2600', '2600', '2600', '2600', '2600', '2600'],
     'Price Date': ['02 May 2021',
      '01 May 2021',
      '02 May 2021',
      '01 May 2021',
      '02 May 2021',
      '01 May 2021']}




```python

```
