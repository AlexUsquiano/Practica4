# Practica4
Conexión a Bases de Datos con JDBC
-- phpMyAdmin SQL Dump
-- version 4.8.5
-- https://www.phpmyadmin.net/
--
-- Servidor: 127.0.0.1
-- Tiempo de generación: 08-06-2020 a las 20:16:10
-- Versión del servidor: 10.1.38-MariaDB
-- Versión de PHP: 7.3.2

SET SQL_MODE = "NO_AUTO_VALUE_ON_ZERO";
SET AUTOCOMMIT = 0;
START TRANSACTION;
SET time_zone = "+00:00";


/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!40101 SET NAMES utf8mb4 */;

--
-- Base de datos: `registro`
--

-- --------------------------------------------------------

--
-- Estructura de tabla para la tabla `persona`
--

CREATE TABLE `persona` (
  `Id` int(20) NOT NULL,
  `Nombres` varchar(100) NOT NULL,
  `Correo` varchar(100) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

--
-- Volcado de datos para la tabla `persona`
--

INSERT INTO `persona` (`Id`, `Nombres`, `Correo`) VALUES
(1, 'admin', '123456');

-- --------------------------------------------------------

--
-- Estructura de tabla para la tabla `usuario`
--

CREATE TABLE `usuario` (
  `Id_Usuario` int(11) NOT NULL,
  `DNI` text NOT NULL,
  `Nombres` text NOT NULL,
  `Fecha` text NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

--
-- Volcado de datos para la tabla `usuario`
--

INSERT INTO `usuario` (`Id_Usuario`, `DNI`, `Nombres`, `Fecha`) VALUES
(19, 'Para nadie es un secreto que la tecnologia ha permeado diversos campos, con un impacto positivo no solo en la rapidez de los procesos, sino tambien en el bienestar del ser humano. La salud no ha sido ajena a esta influencia y hoy son numerosos los procedimientos a los que ha sido aplicada la tecnologia medica: en el diagnostico, seguimiento o tratamiento de enfermedades o condiciones medicas; tambien registros medicos en linea, dispositivos moviles para el tratamiento de dolencias, equipos de diagnostico, procesos automatizados y hasta consultas medicas en Internet se encuentran entre los avances.', 'Tecnologia al servicio de la salud', '05/06/2020'),
(20, 'La pandemia del nuevo coronavirus originada en la ciudad china de Wuhan ha dejado mas de 400.000 victimas mortales y poco mas de siete millones de personas contagiadas en todo el mundo, segun el ultimo balance de la Universidad Johns Hopkins.', 'La pandemia de coronavirus deja mas de 400.000 muertos en todo el mundo', '25/03/2020'),
(21, 'Estados Unidos ha superado este domingo los 110 000 fallecidos por el coronavirus, segun los datos recopilados por la Universidad John Hopkins, que recoge ademas que son 1 928 594 los casos confirmados de la enfermedad. Ademas, destaca que hay 500 849 pacientes recuperados.', 'EE. UU. supera los 110 000 fallecidos por el coronavirus', '09/03/2020');

--
-- Índices para tablas volcadas
--

--
-- Indices de la tabla `persona`
--
ALTER TABLE `persona`
  ADD PRIMARY KEY (`Id`);

--
-- Indices de la tabla `usuario`
--
ALTER TABLE `usuario`
  ADD PRIMARY KEY (`Id_Usuario`);

--
-- AUTO_INCREMENT de las tablas volcadas
--

--
-- AUTO_INCREMENT de la tabla `persona`
--
ALTER TABLE `persona`
  MODIFY `Id` int(20) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=2;

--
-- AUTO_INCREMENT de la tabla `usuario`
--
ALTER TABLE `usuario`
  MODIFY `Id_Usuario` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=22;
COMMIT;

/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION */;
