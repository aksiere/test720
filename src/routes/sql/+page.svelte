<code><pre style="padding: 1rem;">
WITH months AS (SELECT generate_series(1, 12) AS month)
SELECT 
	month as "Месяц", 
	EXTRACT(DAY FROM (date_trunc('month', make_date(2023, month, 1)) + INTERVAL '1 MONTH' - INTERVAL '1 DAY')) AS "Дней в месяце"
FROM 
	months;
</pre></code>