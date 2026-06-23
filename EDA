## 🔎 Analisis Exploratorio de Datos (EDA)

-- Exploratory Data Analysis 

SELECT MAX(Saldo), MAX(Edad)
FROM segmentacion_clientes2;

SELECT *
FROM segmentacion_clientes2
WHERE Saldo >= 6000
ORDER BY Segmento DESC;

SELECT Nombre, SUM(Saldo)
FROM segmentacion_clientes2
GROUP BY Nombre
ORDER BY 2 DESC;

SELECT MIN(FechaRegistro), MAX(FechaRegistro)
FROM segmentacion_clientes2;

SELECT Edad, COUNT(*) AS total_clientes 
FROM segmentacion_clientes2
GROUP BY Edad
ORDER BY Edad DESC;

SELECT Segmento, COUNT(*) AS Clientes 
FROM segmentacion_clientes2
GROUP BY Segmento
ORDER BY Segmento DESC;

SELECT 
	CASE 
		WHEN Edad BETWEEN 18 AND 25 THEN "18-25"
        WHEN Edad BETWEEN 26 AND 35 THEN "26-35"
        WHEN Edad BETWEEN 36 AND 45 THEN "36-45"
        ELSE "46+"
	END AS Rango_edad,
    Segmento,
    COUNT(*) AS Clientes 
FROM segmentacion_clientes2
GROUP BY Rango_edad, Segmento 
ORDER BY Rango_edad, Segmento DESC;

SELECT Saldo, COUNT(*) AS GrandTotal
FROM segmentacion_clientes2
GROUP BY Saldo
ORDER BY Saldo ASC;

SELECT DISTINCT WalletActiva
FROM segmentacion_clientes2;

SELECT WalletActiva, COUNT(*) AS Tarjeta_Activa
FROM segmentacion_clientes2
GROUP BY WalletActiva
ORDER BY WalletActiva DESC;

SELECT WalletActiva, SUM(CASE WHEN Churn = "Si" THEN 1 ELSE 0 END) AS Cliente_Churn,
COUNT(*) AS Total_WA,
ROUND(SUM(CASE WHEN Churn = "Si" THEN 1 ELSE 0 END) * 100 / COUNT(*), 2) AS Tasa_Churn
FROM segmentacion_clientes2
GROUP BY WalletActiva;

SELECT Churn 
FROM segmentacion_clientes2;
