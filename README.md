# dynamic-dependent-select-box
Dynamic dependent select box using jQuery, Ajax, and PHP

## Documentation

[https://www.cluemediator.com/dynamic-dependent-select-box-using-jquery,-ajax,-and-php](https://www.cluemediator.com/dynamic-dependent-select-box-using-jquery,-ajax,-and-php)

## Connect with us

Website: [Clue Mediator](https://www.cluemediator.com)  
Like us on [Facebook](https://www.facebook.com/thecluemediator)  
Follow us on [Twitter](https://twitter.com/cluemediator)  
Join us on [Telegram](https://t.me/cluemediator)




-- phpMyAdmin SQL Dump
-- version 5.0.4
-- https://www.phpmyadmin.net/
--
-- Host: localhost
-- Generation Time: Jun 19, 2021 at 09:37 PM
-- Server version: 10.4.16-MariaDB
-- PHP Version: 7.4.12

SET SQL_MODE = "NO_AUTO_VALUE_ON_ZERO";
START TRANSACTION;
SET time_zone = "+00:00";


/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!40101 SET NAMES utf8mb4 */;

--
-- Database: `ccs_trading`
--

-- --------------------------------------------------------

--
-- Table structure for table `class`
--

CREATE TABLE `class` (
  `id` int(11) NOT NULL,
  `state_id` int(11) NOT NULL,
  `class_name` varchar(255) NOT NULL
) ENGINE=MyISAM DEFAULT CHARSET=utf8mb4;

--
-- Dumping data for table `class`
--

INSERT INTO `class` (`id`, `state_id`, `class_name`) VALUES
(1, 1, 'Class1-9,500'),
(2, 1, 'Class2-10,000'),
(3, 1, 'Class3-11,000'),
(4, 2, 'Class1-10,000'),
(5, 2, 'Class2-10,500'),
(6, 2, 'Class3-11,500'),
(7, 3, 'Class1-9,000'),
(8, 3, 'Class2-9,500'),
(9, 3, 'Class3-10,500'),
(10, 4, 'Class1-9,500'),
(11, 4, 'Class2-10,000'),
(12, 4, 'Class3-11,000');

-- --------------------------------------------------------

--
-- Table structure for table `destination`
--

CREATE TABLE `destination` (
  `id` int(11) NOT NULL,
  `country_id` int(11) NOT NULL,
  `state_name` varchar(255) NOT NULL
) ENGINE=MyISAM DEFAULT CHARSET=utf8mb4;

--
-- Dumping data for table `destination`
--

INSERT INTO `destination` (`id`, `country_id`, `state_name`) VALUES
(1, 1, 'Philippines-Valenzuela'),
(2, 1, 'Philippines-Dasmarinas'),
(3, 2, 'Philippines-Valenzuela'),
(4, 2, 'Philippines-Dasmarinas');

-- --------------------------------------------------------

--
-- Table structure for table `origin`
--

CREATE TABLE `origin` (
  `id` int(11) NOT NULL,
  `country_name` varchar(255) NOT NULL
) ENGINE=MyISAM DEFAULT CHARSET=utf8mb4;

--
-- Dumping data for table `origin`
--

INSERT INTO `origin` (`id`, `country_name`) VALUES
(1, 'China-Yiwu'),
(2, 'China-GuangZhou');

--
-- Indexes for dumped tables
--

--
-- Indexes for table `class`
--
ALTER TABLE `class`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `destination`
--
ALTER TABLE `destination`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `origin`
--
ALTER TABLE `origin`
  ADD PRIMARY KEY (`id`);

--
-- AUTO_INCREMENT for dumped tables
--

--
-- AUTO_INCREMENT for table `class`
--
ALTER TABLE `class`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=18;

--
-- AUTO_INCREMENT for table `destination`
--
ALTER TABLE `destination`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=7;

--
-- AUTO_INCREMENT for table `origin`
--
ALTER TABLE `origin`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=4;
COMMIT;

/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION */;
