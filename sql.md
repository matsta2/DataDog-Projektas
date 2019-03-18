-- phpMyAdmin SQL Dump
-- version 4.7.4
-- https://www.phpmyadmin.net/
--
-- Host: 127.0.0.1
-- Generation Time: 2019 m. Kov 18 d. 22:44
-- Server version: 10.1.28-MariaDB
-- PHP Version: 7.1.11

SET SQL_MODE = "NO_AUTO_VALUE_ON_ZERO";
SET AUTOCOMMIT = 0;
START TRANSACTION;
SET time_zone = "+00:00";


/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!40101 SET NAMES utf8mb4 */;

--
-- Database: `project`
--

-- --------------------------------------------------------

--
-- Sukurta duomenų struktūra lentelei `event`
--

CREATE TABLE `event` (
  `id` int(11) NOT NULL,
  `user_id_id` int(11) NOT NULL,
  `name` varchar(255) COLLATE utf8mb4_unicode_ci NOT NULL,
  `date` datetime NOT NULL,
  `location` varchar(255) COLLATE utf8mb4_unicode_ci NOT NULL,
  `price` double NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci;

--
-- Sukurta duomenų kopija lentelei `event`
--

INSERT INTO `event` (`id`, `user_id_id`, `name`, `date`, `location`, `price`) VALUES
(1, 1, 'Zoozzy', '2018-11-26 00:00:00', 'China', 42.2),
(2, 2, 'Jabberstorm', '2018-09-14 00:00:00', 'Indonesia', 92.2),
(3, 3, 'Vitz', '2018-01-16 00:00:00', 'South Africa', 55.6),
(4, 4, 'Mynte', '2018-02-22 00:00:00', 'Sweden', 39.2),
(5, 5, 'Chatterbridge', '2018-09-15 00:00:00', 'Indonesia', 21.3),
(6, 6, 'Photobug', '2018-10-05 00:00:00', 'Tunisia', 51.7),
(7, 7, 'Rhybox', '2018-09-08 00:00:00', 'Greece', 54.2),
(8, 8, 'Tazzy', '2019-02-28 00:00:00', 'Brazil', 38.9),
(9, 9, 'Vinder', '2018-02-25 00:00:00', 'Czech Republic', 56.4),
(10, 10, 'Chatterbridge', '2017-06-18 00:00:00', 'Peru', 98.9),
(11, 11, 'Cogilith', '2017-11-26 00:00:00', 'Sweden', 36.8),
(12, 12, 'Meedoo', '2017-08-21 00:00:00', 'China', 2.8),
(13, 13, 'Brainsphere', '2017-12-23 00:00:00', 'Zimbabwe', 17.8),
(14, 14, 'Photobean', '2018-12-05 00:00:00', 'Brazil', 79.4),
(15, 15, 'Vimbo', '2018-11-01 00:00:00', 'Philippines', 39),
(16, 16, 'Zoomdog', '2017-05-11 00:00:00', 'Philippines', 67.1),
(17, 17, 'Meejo', '2017-09-10 00:00:00', 'Indonesia', 85.9),
(18, 18, 'Bubblemix', '2017-05-14 00:00:00', 'Brazil', 86),
(19, 19, 'Dabvine', '2017-12-20 00:00:00', 'Vietnam', 36.7),
(20, 20, 'Pixoboo', '2017-10-25 00:00:00', 'Indonesia', 49);

-- --------------------------------------------------------

--
-- Sukurta duomenų struktūra lentelei `migration_versions`
--

CREATE TABLE `migration_versions` (
  `version` varchar(14) COLLATE utf8mb4_unicode_ci NOT NULL,
  `executed_at` datetime NOT NULL COMMENT '(DC2Type:datetime_immutable)'
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci;

--
-- Sukurta duomenų kopija lentelei `migration_versions`
--

INSERT INTO `migration_versions` (`version`, `executed_at`) VALUES
('20190316232723', '2019-03-17 21:52:01'),
('20190317213053', '2019-03-17 21:52:02');

-- --------------------------------------------------------

--
-- Sukurta duomenų struktūra lentelei `user`
--

CREATE TABLE `user` (
  `id` int(11) NOT NULL,
  `username` varchar(180) COLLATE utf8mb4_unicode_ci NOT NULL,
  `roles` longtext COLLATE utf8mb4_unicode_ci NOT NULL COMMENT '(DC2Type:array)',
  `password` varchar(255) COLLATE utf8mb4_unicode_ci NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci;

--
-- Sukurta duomenų kopija lentelei `user`
--

INSERT INTO `user` (`id`, `username`, `roles`, `password`) VALUES
(1, 'user0', 'a:0:{}', '$2y$13$irLKrmgRYlVcioO8v6aphOV5w8trRhYe53S.eoJeygHqjJUTnwbo2'),
(2, 'user1', 'a:0:{}', '$2y$13$wOh91WV7czoN3zL3YiPYkuu3m2nR7I9idUqBUnBwgYaATtnUNuk5G'),
(3, 'user2', 'a:0:{}', '$2y$13$mmD2zRMbrpInM3fZIaul0O2yr/.DAguMj5qbp7aJ9NRZtuW4Eomu.'),
(4, 'user3', 'a:0:{}', '$2y$13$mSft73Nvqhk4n5dDMT4sduKOPTLfWDlx0uBvrxrB9nfdcfqxKKute'),
(5, 'user4', 'a:0:{}', '$2y$13$Z7cwCUYVbzrRdfYSi6Zn8.V1qgEamVceMSOzVebh41kNHpX4cS05O'),
(6, 'user5', 'a:0:{}', '$2y$13$ikuCD5OqaZoOYNp4RKvp8.uVTEM4ELZsqo5.jdSa3rDXz4tcIwaHG'),
(7, 'user6', 'a:0:{}', '$2y$13$H4x84v7R7hc9G4mYIuNuoO1OSbzGPcVxHwxIuBBSgbBkGP8vnztO.'),
(8, 'user7', 'a:0:{}', '$2y$13$Uipdn0IYhZYyo0Q9PDVXGOoaeIp8NQMnRZVTx59i.SHRlFNr1z0gK'),
(9, 'user8', 'a:0:{}', '$2y$13$ILWK3hKc8SMQgwGo36CrI.A59NfDZpsqQZhPwPClUEXofAX7pU4UG'),
(10, 'user9', 'a:0:{}', '$2y$13$YYStO7RtBN61JtTMPB/YW.bWduEguhUJH8CVpY/weJMtQfJmkyUQu'),
(11, 'user10', 'a:0:{}', '$2y$13$eYBHJy6lYNSQK50.kGmdIOImSGJk4e03cx7rdvxEpGh35EqjeEZ0.'),
(12, 'user11', 'a:0:{}', '$2y$13$Re3Hw8xx9tDb9A6d4c7gr.XmkxfdO3geMicVh3ji.C4OAeXL/sAvC'),
(13, 'user12', 'a:0:{}', '$2y$13$PsU27jwXcl3wdUvHeGVQXulY0.FhrjSiN5L.Ukezufyj1XyZqU4ya'),
(14, 'user13', 'a:0:{}', '$2y$13$jOzo/1M44XfUt3zguQDXPefTufHc1tVV4.Dav.L7t/qVt00ZUm3Tm'),
(15, 'user14', 'a:0:{}', '$2y$13$QNyikZhhyO1p2.s3Fky8JO2VnNW4geljGvceYRXnpG7mhU0LJPubq'),
(16, 'user15', 'a:0:{}', '$2y$13$MqocSwoIKrIlZeT5wTxRXORLVP71/epW84jACRiC4Dx6gS5qnZv0G'),
(17, 'user16', 'a:0:{}', '$2y$13$fg.rc3BCXsDNxmUopydmx.LyHkKygCkBwaJ6UCGhGOGmk3Uint3sq'),
(18, 'user17', 'a:0:{}', '$2y$13$1fPTUYV6Eg86oa72WBNvw.1KC9iP8mr8AGSR/XNkNDA3Oy7W6c1yu'),
(19, 'user18', 'a:0:{}', '$2y$13$USY20BAKorlVDjRIgt1THOsDuCf3VUHrUSU1KLO0IaxbYBwzpmZHm'),
(20, 'user19', 'a:0:{}', '$2y$13$TQUzeuaKDhOIfAzVH4Q3vuuMhchTqBr7YCzIxXGzB76yBx.9rbreC');

--
-- Indexes for dumped tables
--

--
-- Indexes for table `event`
--
ALTER TABLE `event`
  ADD PRIMARY KEY (`id`),
  ADD KEY `IDX_3BAE0AA79D86650F` (`user_id_id`);

--
-- Indexes for table `migration_versions`
--
ALTER TABLE `migration_versions`
  ADD PRIMARY KEY (`version`);

--
-- Indexes for table `user`
--
ALTER TABLE `user`
  ADD PRIMARY KEY (`id`),
  ADD UNIQUE KEY `UNIQ_8D93D649F85E0677` (`username`);

--
-- AUTO_INCREMENT for dumped tables
--

--
-- AUTO_INCREMENT for table `event`
--
ALTER TABLE `event`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=21;

--
-- AUTO_INCREMENT for table `user`
--
ALTER TABLE `user`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=21;

--
-- Apribojimai eksportuotom lentelėm
--

--
-- Apribojimai lentelei `event`
--
ALTER TABLE `event`
  ADD CONSTRAINT `FK_3BAE0AA79D86650F` FOREIGN KEY (`user_id_id`) REFERENCES `user` (`id`);
COMMIT;

/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION */;