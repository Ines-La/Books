# Books
-- phpMyAdmin SQL Dump
-- version 4.8.3
-- https://www.phpmyadmin.net/
--
-- Hôte : 127.0.0.1
-- Généré le :  mer. 08 juil. 2020 à 15:08
-- Version du serveur :  10.1.36-MariaDB
-- Version de PHP :  7.2.11

SET SQL_MODE = "NO_AUTO_VALUE_ON_ZERO";
SET AUTOCOMMIT = 0;
START TRANSACTION;
SET time_zone = "+00:00";


/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!40101 SET NAMES utf8mb4 */;

--
-- Base de données :  `projet`
--

-- --------------------------------------------------------

--
-- Structure de la table `information`
--

CREATE TABLE `information` (
  `ID` int(30) NOT NULL,
  `state` text
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

--
-- Déchargement des données de la table `information`
--

INSERT INTO `information` (`ID`, `state`) VALUES
(65465465, 'Paid'),
(65855465, 'paid'),
(65855466, 'not_paid'),
(65855857, 'not_paid'),
(72655465, 'not_paid'),
(72855465, 'paid'),
(75355465, 'paid'),
(78855465, 'paid');

-- --------------------------------------------------------

--
-- Structure de la table `students`
--

CREATE TABLE `students` (
  `ID` int(30) NOT NULL,
  `Name` text,
  `Last Name` text,
  `Phone number` int(30) DEFAULT NULL,
  `Email` varchar(30) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

--
-- Déchargement des données de la table `students`
--

INSERT INTO `students` (`ID`, `Name`, `Last Name`, `Phone number`, `Email`) VALUES
(65465465, 'Ines', 'Lachheb', 8569365, 'ineskk@gmail.com'),
(65855465, 'oumaima', 'Naoui', 2369365, 'oumaimakk@gmail.com'),
(65855466, 'Alia', 'Chbeb', 8569723, 'alia55@gmail.com'),
(65855857, 'Rihem', 'Jaafoura', 2547485, 'rihem85@gmail.com');

-- --------------------------------------------------------

--
-- Structure de la table `teachers`
--

CREATE TABLE `teachers` (
  `ID teacher` int(30) NOT NULL,
  `First name` text,
  `Last name` text,
  `Phone number` int(30) DEFAULT NULL,
  `Email` varchar(30) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

--
-- Déchargement des données de la table `teachers`
--

INSERT INTO `teachers` (`ID teacher`, `First name`, `Last name`, `Phone number`, `Email`) VALUES
(72655465, 'Ousema', 'Rkik', 2458759, 'Rkikouss@gmail.com'),
(72855465, 'Omar', 'Triki', 2589658, 'trikiomar@gmail.com'),
(75355465, 'Rim', 'Slema', 5869325, 'Rimme@gmail.com'),
(78855465, 'Islem', 'Tayeb', 2587468, 'Tayeb58@gmail.com');

--
-- Index pour les tables déchargées
--

--
-- Index pour la table `information`
--
ALTER TABLE `information`
  ADD PRIMARY KEY (`ID`),
  ADD KEY `ID` (`ID`);

--
-- Index pour la table `students`
--
ALTER TABLE `students`
  ADD PRIMARY KEY (`ID`);

--
-- Index pour la table `teachers`
--
ALTER TABLE `teachers`
  ADD PRIMARY KEY (`ID teacher`);
COMMIT;

/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION */;
