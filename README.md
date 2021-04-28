#DE. Home work #3. Data quality with great expectations framework

### dtirskikh.ods_billing ###

---user_id

#Не должно быть данных с NULL c логической и бизнес точки зрения
batch.expect_column_values_to_not_be_null(column='user_id')

#Проверка на тип данных
batch.expect_column_values_to_be_of_type(column='user_id', type_='BIGINT')

-billing_period

#Не должно быть данных с NULL c логической и бизнес точки зрения
batch.expect_column_values_to_not_be_null(column='billing_period')

#Проверка на тип данных
batch.expect_column_values_to_be_of_type(column='billing_period', type_='DATE')

#Проверка на то, что данные попадают в заданный диапазон
batch.expect_column_values_to_be_between(column='billing_period', max_value='2022-01-01', min_value='2012-01-01')

---
