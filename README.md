# DE. Home work #5. Data quality with great expectations framework #

# dtirskikh.ods_traffic #

- Не должно быть данных с NULL c логической и бизнес точки зрения  
batch.expect_column_values_to_not_be_null(column='user_id')

- Проверка на тип данных  
batch.expect_column_values_to_be_of_type(column='user_id', type_='BIGINT')  

## timestamp_ ## 

- Не должно быть данных с NULL c логической и бизнес точки зрения  
batch.expect_column_values_to_not_be_null(column='timestamp_')

- Проверка на тип данных  
batch.expect_column_values_to_be_of_type(column='timestamp_', type_='TIMESTAMP')

- Проверка на то, что данные попадают в заданный диапазон  
batch.expect_column_values_to_be_between(column='timestamp_', max_value='2021-01-01', min_value='2012-01-01')

## device_id ## 

- Не должно быть данных с NULL c логической и бизнес точки зрения  
batch.expect_column_values_to_not_be_null(column='device_id')

- Проверка на тип данных  
batch.expect_column_values_to_be_of_type(column='device_id', type_='TEXT')

- Все значения столбца должны соответствовать регулярному выражению  
batch.expect_column_values_to_match_regex(column='device_id', regex='^d\d{3}$')

## device_ip_addr ## 

- Не должно быть данных с NULL c логической и бизнес точки зрения  
batch.expect_column_values_to_not_be_null(column='device_ip_addr')

- Проверка на тип данных  
batch.expect_column_values_to_be_of_type(column='device_ip_addr', type_='TEXT')

- Все значения столбца должны соответствовать регулярному выражению  
batch.expect_column_values_to_match_regex(column='device_ip_addr', regex='^((25[0-5]|(2[0-4]|1[0-9]|[1-9]|)[0-9])(\.(?!$)|$)){4}$')

## bytes_received ## 

- Проверка на тип данных  
batch.expect_column_values_to_be_of_type(column='bytes_received', type_='BIGINT')

## bytes_sent ## 

- Проверка на тип данных  
batch.expect_column_values_to_be_of_type(column='bytes_sent', type_='BIGINT')

# dtirskikh.ods_payment #

## user_id ## 

- Не должно быть данных с NULL c логической и бизнес точки зрения  
batch.expect_column_values_to_not_be_null(column='user_id')

- Проверка на тип данных  
batch.expect_column_values_to_be_of_type(column='user_id', type_='BIGINT')

## pay_doc_type ## 

- Не должно быть данных с NULL c логической и бизнес точки зрения  
batch.expect_column_values_to_not_be_null(column='pay_doc_type')

- Проверка на тип данных  
batch.expect_column_values_to_be_of_type(column='pay_doc_type', type_='TEXT')

- Соответствие значения допустимому списку  
batch.expect_column_distinct_values_to_be_in_set(column='pay_doc_type', value_set=['MASTER', 'MIR', 'VISA'])

- В датасете должны присутствовать все значения из списка  
batch.expect_column_distinct_values_to_equal_set(column='pay_doc_type', value_set=['MASTER', 'MIR', 'VISA'])

## pay_doc_num ## 

- Не должно быть данных с NULL c логической и бизнес точки зрения  
batch.expect_column_values_to_not_be_null(column='pay_doc_num')

- Проверка на тип данных  
batch.expect_column_values_to_be_of_type(column='pay_doc_num', type_='BIGINT')

## account ## 

- Не должно быть данных с NULL c логической и бизнес точки зрения  
batch.expect_column_values_to_not_be_null(column='account')

- Проверка на тип данных  
batch.expect_column_values_to_be_of_type(column='account', type_='TEXT')

- Все значения столбца должны соответствовать регулярному выражению  
batch.expect_column_values_to_match_regex(column='account', regex='^FL-\d+$')

## phone ## 

- Проверка на тип данных  
batch.expect_column_values_to_be_of_type(column='phone', type_='TEXT')

- Все значения столбца должны соответствовать регулярному выражению  
batch.expect_column_values_to_match_regex(column='phone', regex='^(\+7)?[\s\-]?\(?[489][0-9]{2}\)?[\s\-]?[0-9]{3}[\s\-]?[0-9]{2}[\s\-]?[0-9]{2}$')

## billing_period ## 

- Не должно быть данных с NULL c логической и бизнес точки зрения  
batch.expect_column_values_to_not_be_null(column='billing_period')

- Проверка на тип данных  
batch.expect_column_values_to_be_of_type(column='billing_period', type_='DATE')

- Проверка на то, что данные попадают в заданный диапазон  
batch.expect_column_values_to_be_between(column='billing_period', max_value='2022-01-01', min_value='2012-01-01')

## pay_date ## 

- Не должно быть данных с NULL c логической и бизнес точки зрения  
batch.expect_column_values_to_not_be_null(column='pay_date')

- Проверка на тип данных  
batch.expect_column_values_to_be_of_type(column='pay_date', type_='TIMESTAMP')

- Проверка на то, что данные попадают в заданный диапазон  
batch.expect_column_values_to_be_between(column='pay_date', max_value='2021-01-01', min_value='2012-01-01')

# dtirskikh.ods_billing #

## user_id ## 

- Не должно быть данных с NULL c логической и бизнес точки зрения  
batch.expect_column_values_to_not_be_null(column='user_id')

- Проверка на тип данных  
batch.expect_column_values_to_be_of_type(column='user_id', type_='BIGINT')

## billing_period ## 

- Не должно быть данных с NULL c логической и бизнес точки зрения  
batch.expect_column_values_to_not_be_null(column='billing_period')

- Проверка на тип данных  
batch.expect_column_values_to_be_of_type(column='billing_period', type_='DATE')

- Проверка на то, что данные попадают в заданный диапазон  
batch.expect_column_values_to_be_between(column='billing_period', max_value='2022-01-01', min_value='2012-01-01')

## service ## 

- Не должно быть данных с NULL c логической и бизнес точки зрения  
batch.expect_column_values_to_not_be_null(column='service')

- Проверка на тип данных  
batch.expect_column_values_to_be_of_type(column='service', type_='TEXT')

- Соответствие значения допустимому списку  
batch.expect_column_distinct_values_to_be_in_set(column='service', value_set=['Connect', 'Disconnect', 'Setup Environment'])

## tariff ## 

- Не должно быть данных с NULL c логической и бизнес точки зрения  
batch.expect_column_values_to_not_be_null(column='tariff')

- Проверка на тип данных  
batch.expect_column_values_to_not_be_null(column='tariff')

- Соответствие значения допустимому списку  
batch.expect_column_distinct_values_to_be_in_set(column='tariff', value_set=['Maxi', 'Mini', 'Gigabyte', 'Megabyte'])

## sum ## 

- Не должно быть данных с NULL c логической и бизнес точки зрения  
batch.expect_column_values_to_not_be_null(column='sum')

- Проверка на тип данных  
batch.expect_column_values_to_be_of_type(column='sum', type_='NUMERIC')

- Проверка на то, что данные попадают в заданный диапазон  
batch.expect_column_values_to_be_between(column='sum', max_value=5000, min_value=0)

## created_at ## 

- Не должно быть данных с NULL c логической и бизнес точки зрения  
batch.expect_column_values_to_not_be_null(column='created_at')

- Проверка на тип данных  
batch.expect_column_values_to_be_of_type(column='created_at', type_='DATE')

- Проверка на то, что данные попадают в заданный диапазон  
batch.expect_column_values_to_be_between(column='created_at', max_value='2022-01-01', min_value='2012-01-01')


# dtirskikh.ods_issue #

## user_id ## 

- Не должно быть данных с NULL c логической и бизнес точки зрения  
batch.expect_column_values_to_not_be_null(column='user_id')

- Проверка на тип данных  
batch.expect_column_values_to_be_of_type(column='user_id', type_='BIGINT')

## start_time ## 

- Не должно быть данных с NULL c логической и бизнес точки зрения  
batch.expect_column_values_to_not_be_null(column='start_time')

- Проверка на тип данных  
batch.expect_column_values_to_be_of_type(column='start_time', type_='TIMESTAMP')

- Проверка на то, что данные попадают в заданный диапазон  
batch.expect_column_values_to_be_between(column='start_time', max_value='2022-01-01', min_value='2012-01-01')

## end_time ## 

- Не должно быть данных с NULL c логической и бизнес точки зрения  
batch.expect_column_values_to_not_be_null(column='end_time')

- Проверка на тип данных  
batch.expect_column_values_to_be_of_type(column='end_time', type_='TIMESTAMP')

- Проверка на то, что данные попадают в заданный диапазон  
batch.expect_column_values_to_be_between(column='end_time', max_value='2022-01-01', min_value='2012-01-01')

## title ## 

- Не должно быть данных с NULL c логической и бизнес точки зрения  
batch.expect_column_values_to_not_be_null(column='title')

- Проверка на тип данных  
batch.expect_column_values_to_be_of_type(column='title', type_='TEXT')


## description ## 

- Не должно быть данных с NULL c логической и бизнес точки зрения  
batch.expect_column_values_to_not_be_null(column='description')

- Проверка на тип данных  
batch.expect_column_values_to_be_of_type(column='description', type_='TEXT')

## service ## 

- Не должно быть данных с NULL c логической и бизнес точки зрения  
batch.expect_column_values_to_not_be_null(column='service')

- Проверка на тип данных  
batch.expect_column_values_to_be_of_type(column='service', type_='TEXT')

- Соответствие значения допустимому списку  
batch.expect_column_distinct_values_to_be_in_set(column='service', value_set=['Connect', 'Disconnect', 'Setup Environment'])

