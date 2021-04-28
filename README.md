#DE. Home work #3. Data quality with great expectations framework

### dtirskikh.ods_billing ###

---user_id

#Не должно быть данных с NULL c логической и бизнес точки зрения
batch.expect_column_values_to_not_be_null(column='user_id')

#Проверка на тип данных
batch.expect_column_values_to_be_of_type(column='user_id', type_='BIGINT')

---billing_period

#Не должно быть данных с NULL c логической и бизнес точки зрения
batch.expect_column_values_to_not_be_null(column='billing_period')

#Проверка на тип данных
batch.expect_column_values_to_be_of_type(column='billing_period', type_='DATE')

#Проверка на то, что данные попадают в заданный диапазон
batch.expect_column_values_to_be_between(column='billing_period', max_value='2022-01-01', min_value='2012-01-01')

---service

#Не должно быть данных с NULL c логической и бизнес точки зрения
batch.expect_column_values_to_not_be_null(column='service')

#Проверка на тип данных
batch.expect_column_values_to_be_of_type(column='service', type_='TEXT')

#Соответствие значения допустимому списку
batch.expect_column_distinct_values_to_be_in_set(column='service', value_set=['Connect', 'Disconnect', 'Setup Environment'])

---tariff

#Не должно быть данных с NULL c логической и бизнес точки зрения
batch.expect_column_values_to_not_be_null(column='tariff')

#Проверка на тип данных
batch.expect_column_values_to_not_be_null(column='tariff')

#Соответствие значения допустимому списку
batch.expect_column_distinct_values_to_be_in_set(column='tariff', value_set=['Maxi', 'Mini', 'Gigabyte', 'Megabyte'])

---sum

#Не должно быть данных с NULL c логической и бизнес точки зрения
batch.expect_column_values_to_not_be_null(column='sum')

#Проверка на тип данных
batch.expect_column_values_to_be_of_type(column='sum', type_='NUMERIC')

#Проверка на то, что данные попадают в заданный диапазон
batch.expect_column_values_to_be_between(column='sum', max_value=5000, min_value=0)

---created_at

#Не должно быть данных с NULL c логической и бизнес точки зрения
batch.expect_column_values_to_not_be_null(column='created_at')

#Проверка на тип данных
batch.expect_column_values_to_be_of_type(column='created_at', type_='DATE')

#Проверка на то, что данные попадают в заданный диапазон
batch.expect_column_values_to_be_between(column='created_at', max_value='2022-01-01', min_value='2012-01-01')


### dtirskikh.ods_issue ###

---user_id

#Не должно быть данных с NULL c логической и бизнес точки зрения
batch.expect_column_values_to_not_be_null(column='user_id')

#Проверка на тип данных
batch.expect_column_values_to_be_of_type(column='user_id', type_='BIGINT')

---start_time

#Не должно быть данных с NULL c логической и бизнес точки зрения
batch.expect_column_values_to_not_be_null(column='start_time')

#Проверка на тип данных
batch.expect_column_values_to_be_of_type(column='start_time', type_='TIMESTAMP')

#Проверка на то, что данные попадают в заданный диапаз
batch.expect_column_values_to_be_between(column='start_time', max_value='2022-01-01', min_value='2012-01-01')

---end_time

#Не должно быть данных с NULL c логической и бизнес точки зрения
batch.expect_column_values_to_not_be_null(column='end_time')

#Проверка на тип данных
batch.expect_column_values_to_be_of_type(column='end_time', type_='TIMESTAMP')

#Проверка на то, что данные попадают в заданный диапаз
batch.expect_column_values_to_be_between(column='end_time', max_value='2022-01-01', min_value='2012-01-01')

---title

#Не должно быть данных с NULL c логической и бизнес точки зрения
batch.expect_column_values_to_not_be_null(column='title')

#Проверка на тип данных
batch.expect_column_values_to_be_of_type(column='title', type_='TEXT')


---description

#Не должно быть данных с NULL c логической и бизнес точки зрения
batch.expect_column_values_to_not_be_null(column='description')

#Проверка на тип данных
batch.expect_column_values_to_be_of_type(column='description', type_='TEXT')

---description

#Не должно быть данных с NULL c логической и бизнес точки зрения
batch.expect_column_values_to_not_be_null(column='service')

#Проверка на тип данных
batch.expect_column_values_to_be_of_type(column='service', type_='TEXT')

#Соответствие значения допустимому списку
batch.expect_column_distinct_values_to_be_in_set(column='service', value_set=['Connect', 'Disconnect', 'Setup Environment'])

