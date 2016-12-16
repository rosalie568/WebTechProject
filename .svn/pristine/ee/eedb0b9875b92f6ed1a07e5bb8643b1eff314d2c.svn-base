-- phpMyAdmin SQL Dump
-- version 3.4.11.1deb2+deb7u1
-- http://www.phpmyadmin.net
--
-- Host: localhost
-- Generation Time: May 05, 2015 at 11:10 PM
-- Server version: 5.5.43
-- PHP Version: 5.4.39-0+deb7u2

SET SQL_MODE="NO_AUTO_VALUE_ON_ZERO";
SET time_zone = "+00:00";


/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!40101 SET NAMES utf8 */;

--
-- Database: `th3g`
--

-- --------------------------------------------------------

--
-- Table structure for table `friendList`
--

CREATE TABLE IF NOT EXISTS `friendList` (
  `email` varchar(99) NOT NULL,
  `contactEmail` varchar(99) NOT NULL,
  PRIMARY KEY (`email`,`contactEmail`),
  UNIQUE KEY `email` (`email`),
  UNIQUE KEY `contactEmail` (`contactEmail`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

-- --------------------------------------------------------

--
-- Table structure for table `gameLocations`
--

CREATE TABLE IF NOT EXISTS `gameLocations` (
  `locationId` int(50) NOT NULL AUTO_INCREMENT COMMENT 'id of game',
  `gameLocation` varchar(70) NOT NULL COMMENT 'location of the game',
  PRIMARY KEY (`locationId`)
) ENGINE=InnoDB  DEFAULT CHARSET=latin1 AUTO_INCREMENT=4 ;

--
-- Dumping data for table `gameLocations`
--

INSERT INTO `gameLocations` (`locationId`, `gameLocation`) VALUES
(1, 'Murphy Center'),
(2, 'Murfreesboro YMCA'),
(3, 'Patterson Park Community Center');

-- --------------------------------------------------------

--
-- Table structure for table `gameName`
--

CREATE TABLE IF NOT EXISTS `gameName` (
  `gameId` int(100) NOT NULL AUTO_INCREMENT,
  `createdBy` varchar(50) NOT NULL COMMENT 'who created game?',
  `gameTime` varchar(17) NOT NULL COMMENT 'year/month/day dd:dd',
  `location` varchar(70) NOT NULL COMMENT 'location of game',
  `playersRegistered` int(30) NOT NULL DEFAULT '1' COMMENT '# of players registered for each game',
  PRIMARY KEY (`gameId`)
) ENGINE=InnoDB  DEFAULT CHARSET=latin1 AUTO_INCREMENT=15 ;

--
-- Dumping data for table `gameName`
--

INSERT INTO `gameName` (`gameId`, `createdBy`, `gameTime`, `location`, `playersRegistered`) VALUES
(1, 'rosalie568@hotmail.com', '2015/05/15 21:00', 'Murphy Center', 1),
(5, 'efmo1126@gmail.com', '2015/05/06 20:00', 'Murphy Center', 3),
(7, 'rosalie568@hotmail.com', '2015/05/30 05:00', 'Murfreesboro YMCA', 1),
(8, 'rosalie568@hotmail.com', '2015/06/02 01:00', 'Murfreesboro YMCA', 1),
(9, 'rosalie568@hotmail.com', '2015/05/27 11:00', 'Patterson Park Community Center', 2),
(14, 'hwk568@hotmail.com', '2015/04/28 18:00', 'Patterson Park Community Center', 1);

-- --------------------------------------------------------

--
-- Table structure for table `gameRegistered`
--

CREATE TABLE IF NOT EXISTS `gameRegistered` (
  `gameId` int(100) NOT NULL AUTO_INCREMENT COMMENT 'starts at 1 and increments by 1',
  `playerFirstName` varchar(32) DEFAULT NULL COMMENT 'no more than 32 characters',
  `playerLastName` varchar(32) DEFAULT NULL COMMENT 'no more than 32 characters',
  `playerEmail` varchar(99) NOT NULL COMMENT 'no more than 99 characters',
  PRIMARY KEY (`gameId`,`playerEmail`)
) ENGINE=InnoDB  DEFAULT CHARSET=latin1 AUTO_INCREMENT=15 ;

--
-- Dumping data for table `gameRegistered`
--

INSERT INTO `gameRegistered` (`gameId`, `playerFirstName`, `playerLastName`, `playerEmail`) VALUES
(1, 'Tiffany', 'Hawkins', 'rosalie568@hotmail.com'),
(5, 'Eddy', 'Molina', 'efmo1126@gmail.com'),
(5, 'a', 'a', 'hwk568@hotmail.com'),
(5, 'Tiffany', 'Hawkins', 'rosalie568@hotmail.com'),
(7, 'Tiffany', 'Hawkins', 'rosalie568@hotmail.com'),
(8, 'Tiffany', 'Hawkins', 'rosalie568@hotmail.com'),
(9, 'a', 'a', 'hwk568@hotmail.com'),
(9, 'Tiffany', 'Hawkins', 'rosalie568@hotmail.com'),
(14, 'a', 'a', 'hwk568@hotmail.com');

-- --------------------------------------------------------

--
-- Table structure for table `numPlayers`
--

CREATE TABLE IF NOT EXISTS `numPlayers` (
  `minPlayers` int(11) NOT NULL DEFAULT '1' COMMENT 'Minimum # of players',
  `maxPlayers` int(11) NOT NULL DEFAULT '30' COMMENT 'Max # of players'
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

--
-- Dumping data for table `numPlayers`
--

INSERT INTO `numPlayers` (`minPlayers`, `maxPlayers`) VALUES
(1, 50);

-- --------------------------------------------------------

--
-- Table structure for table `student`
--

CREATE TABLE IF NOT EXISTS `student` (
  `firstName` varchar(32) NOT NULL COMMENT 'no more than 32 characters',
  `lastName` varchar(32) NOT NULL COMMENT 'no more than 32 characters',
  `email` varchar(99) NOT NULL COMMENT 'maximum of 99 characters',
  `password` varchar(30) NOT NULL COMMENT 'no more thean 30 characters',
  `phoneNum` varchar(14) DEFAULT NULL COMMENT 'format is ddd ddd-dddd',
  `status` varchar(30) NOT NULL DEFAULT 'student' COMMENT 'person is student or admin?',
  PRIMARY KEY (`email`),
  UNIQUE KEY `email` (`email`),
  UNIQUE KEY `password` (`password`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

--
-- Dumping data for table `student`
--

INSERT INTO `student` (`firstName`, `lastName`, `email`, `password`, `phoneNum`, `status`) VALUES
('admin', 'admin', 'admin@mtsu.edu', 'admin', '', 'admin'),
('Eddy', 'Molina', 'efmo1126@gmail.com', 'messi1126', '', 'student'),
('a', 'a', 'hwk568@hotmail.com', 'a', '', 'student'),
('mena', 'estany', 'jyoo@mtsu.edu', 'qwe', '615 686-6893', 'student'),
('Tiffany', 'Hawkins', 'rosalie568@hotmail.com', 'happy', '123 123-1244', 'student');

/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION */;
