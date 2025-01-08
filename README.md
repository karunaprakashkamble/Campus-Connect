# Campus-Connect
-- phpMyAdmin SQL Dump
-- version 5.0.2
-- https://www.phpmyadmin.net/
--
-- Host: 127.0.0.1:3306
-- Generation Time: Nov 19, 2024 at 05:25 PM
-- Server version: 5.7.31
-- PHP Version: 7.3.21

SET SQL_MODE = "NO_AUTO_VALUE_ON_ZERO";
START TRANSACTION;
SET time_zone = "+00:00";


/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!40101 SET NAMES utf8mb4 */;

--
-- Database: `miniproject1`
--

-- --------------------------------------------------------

--
-- Table structure for table `admin`
--

DROP TABLE IF EXISTS `admin`;
CREATE TABLE IF NOT EXISTS `admin` (
  `id` int(20) NOT NULL,
  `username` varchar(20) NOT NULL,
  `password` varchar(20) NOT NULL,
  `email` varchar(30) NOT NULL
) ENGINE=MyISAM DEFAULT CHARSET=latin1;

--
-- Dumping data for table `admin`
--

INSERT INTO `admin` (`id`, `username`, `password`, `email`) VALUES
(1, 'Shruti', 'Shruti01', 'shrutipote1214@gmail.com');

-- --------------------------------------------------------

--
-- Table structure for table `applicants`
--

DROP TABLE IF EXISTS `applicants`;
CREATE TABLE IF NOT EXISTS `applicants` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `full_name` varchar(255) NOT NULL,
  `email` varchar(255) NOT NULL,
  `current_year` int(11) NOT NULL,
  `cgpa` decimal(3,2) NOT NULL,
  `backlogs` varchar(11) NOT NULL,
  `resume_path` varchar(255) NOT NULL,
  `jobtitle` varchar(255) NOT NULL,
  PRIMARY KEY (`id`)
) ENGINE=MyISAM AUTO_INCREMENT=6 DEFAULT CHARSET=latin1;

--
-- Dumping data for table `applicants`
--

INSERT INTO `applicants` (`id`, `full_name`, `email`, `current_year`, `cgpa`, `backlogs`, `resume_path`, `jobtitle`) VALUES
(1, 'Shruti Pote', 'poteshruti12@gmail.com', 3, '9.10', 'NO', 'uploads/ShrutiPote.pdf', 'TCS'),
(3, 'Prerana Shte', 'preranashete@gmail.com', 3, '9.20', 'NO', 'uploads/INTER-PROCESS.pdf', 'Infosys'),
(4, 'abc', 'abc@gmail.com', 4, '8.70', '1', 'uploads/ISE1Component1-Assignment.pdf', 'TCS'),
(5, 'Shruti Pote', 'spote@gmail.com', 4, '8.50', 'NO', 'uploads/YellowandBlackSoftDesignerCreativeModernResume.pdf', 'Infosys');

-- --------------------------------------------------------

--
-- Table structure for table `applied_user`
--

DROP TABLE IF EXISTS `applied_user`;
CREATE TABLE IF NOT EXISTS `applied_user` (
  `ID` int(10) NOT NULL,
  `prn` int(20) NOT NULL,
  `Name` int(30) NOT NULL,
  `email` int(30) NOT NULL,
  `phone_no` int(10) NOT NULL,
  `Status` int(2) NOT NULL
) ENGINE=MyISAM DEFAULT CHARSET=latin1;

-- --------------------------------------------------------

--
-- Table structure for table `job_post`
--

DROP TABLE IF EXISTS `job_post`;
CREATE TABLE IF NOT EXISTS `job_post` (
  `id_jobpost` int(10) NOT NULL AUTO_INCREMENT,
  `jobtitle` varchar(30) NOT NULL,
  `description` varchar(1000) NOT NULL,
  `Location` varchar(50) NOT NULL,
  `minimumsalary` bigint(30) NOT NULL,
  `maximumsalary` bigint(30) NOT NULL,
  `experience` varchar(100) NOT NULL,
  `qualification` varchar(50) NOT NULL,
  `image` varchar(191) DEFAULT NULL,
  PRIMARY KEY (`id_jobpost`)
) ENGINE=MyISAM AUTO_INCREMENT=5 DEFAULT CHARSET=latin1;

--
-- Dumping data for table `job_post`
--

INSERT INTO `job_post` (`id_jobpost`, `jobtitle`, `description`, `Location`, `minimumsalary`, `maximumsalary`, `experience`, `qualification`, `image`) VALUES
(1, 'TCS', '<p><span style=\"color: rgb(30, 34, 60); font-family: proxima-nova, Arial, sans-serif; font-size: 14px;\">Responsible for supervising, managing and motivating a team of Business Development Managers and Inside <b>Sales Team</b> to achieve revenue targets by assigning team goals</span><br></p>', 'Pune', 1500000, 200000, 'HR', 'B.Tech/MCA/M.Sc', 'uploads/tcs.png'),
(2, 'Microsoft', '<p><span style=\"font-weight: bold; color: rgb(188, 192, 195); font-family: arial, sans-serif; font-size: 14px; background-color: rgb(32, 33, 36);\">Consulting and customer support</span><span style=\"color: rgb(189, 193, 198); font-family: arial, sans-serif; font-size: 14px; background-color: rgb(32, 33, 36);\">&nbsp;Â· Corporate and shared services Â· Design and creative Â· Engineering, development, and services</span><br></p>', 'Bangalore', 4000000, 5000000, 'Senior developer', 'MTech', 'uploads/Microsoft-Windows-Phone.png'),
(3, 'IBM', '<p><span style=\"color: rgb(22, 22, 22); font-family: &quot;IBM Plex Sans&quot;, &quot;Helvetica Neue&quot;, Arial, sans-serif;\">When you join IBM, you join a culture of openness, collaboration and trust. You join a team of IBMers who are bringing change into the world â€” helping cure diseases, clean our oceans and make technology work for good.</span><br></p>', 'Bangalore', 500000, 600000, 'Fresher', 'BTech', 'uploads/download (1).png'),
(4, 'Infosys', '<p><span style=\"color: rgb(126, 126, 126); font-family: myriadProRegular; white-space-collapse: preserve;\">To lead Network monitoring and complex troubleshooting activities over supported network/IT Infrastructure covering multi-vendor and multi-site large enterprise environment. 	Lead all critical P1/P2 incidents reported by business and collaborate with other technical SMEs on all incidents affecting production systems.</span><br></p>', 'Mumbai', 1000000, 1200000, 'Software Engineer', 'ME', 'uploads/download (3).png');

-- --------------------------------------------------------

--
-- Table structure for table `notice`
--

DROP TABLE IF EXISTS `notice`;
CREATE TABLE IF NOT EXISTS `notice` (
  `subject` varchar(200) NOT NULL,
  `date1` date NOT NULL,
  `time1` time(6) NOT NULL,
  `Resumepath` varchar(255) NOT NULL
) ENGINE=MyISAM DEFAULT CHARSET=latin1;

--
-- Dumping data for table `notice`
--

INSERT INTO `notice` (`subject`, `date1`, `time1`, `Resumepath`) VALUES
('TCS is coming for campus hiring', '2023-12-10', '10:00:00.000000', 'uploads/Online-Examination-System_All-open.pdf'),
('Exciting news for students.TPO is going to take a session for career development', '2023-12-02', '15:00:00.000000', 'uploads/AWS_Academy_Graduate___AWS_Academy_Cloud_Foundations_Badge20231012-45-n460iv.pdf');

-- --------------------------------------------------------

--
-- Table structure for table `placed_student`
--

DROP TABLE IF EXISTS `placed_student`;
CREATE TABLE IF NOT EXISTS `placed_student` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `name` varchar(30) NOT NULL,
  `package` varchar(20) NOT NULL,
  `company_name` varchar(30) NOT NULL,
  `image` varchar(191) DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=MyISAM AUTO_INCREMENT=5 DEFAULT CHARSET=latin1;

--
-- Dumping data for table `placed_student`
--

INSERT INTO `placed_student` (`id`, `name`, `package`, `company_name`, `image`) VALUES
(1, 'Shradhha Aadekar', '15LPA', 'TCS', 'uploads/emp1 (2).jpg'),
(2, 'Rohit Sharma', '20LPA', 'Cloud4C', 'uploads/emp.png'),
(3, 'Prajakata Aambe', '10LPA', 'IBM', 'uploads/emp2.png'),
(4, 'Om Patil', '5LPA', 'Wipro', 'uploads/profile.jpg');

-- --------------------------------------------------------

--
-- Table structure for table `registered_user`
--

DROP TABLE IF EXISTS `registered_user`;
CREATE TABLE IF NOT EXISTS `registered_user` (
  `ID` int(20) NOT NULL,
  `prn` varchar(20) NOT NULL,
  `Name` varchar(50) NOT NULL,
  `email` varchar(30) NOT NULL,
  `phone_no` varchar(10) NOT NULL,
  `Status` int(2) NOT NULL,
  `dob` varchar(255) DEFAULT NULL,
  `stream` varchar(255) DEFAULT NULL,
  `skills` varchar(255) DEFAULT NULL,
  `aboutme` text,
  `address` varchar(255) DEFAULT NULL,
  `hsc` varchar(50) DEFAULT NULL,
  `ssc` varchar(50) DEFAULT NULL,
  `ug` varchar(255) DEFAULT NULL,
  `pg` varchar(255) DEFAULT NULL,
  `resumepath` varchar(255) DEFAULT NULL,
  `hg` varchar(255) DEFAULT NULL,
  `password` varchar(255) NOT NULL
) ENGINE=MyISAM DEFAULT CHARSET=latin1;

--
-- Dumping data for table `registered_user`
--

INSERT INTO `registered_user` (`ID`, `prn`, `Name`, `email`, `phone_no`, `Status`, `dob`, `stream`, `skills`, `aboutme`, `address`, `hsc`, `ssc`, `ug`, `pg`, `resumepath`, `hg`, `password`) VALUES
(1, '2223010110', 'Shruti Pote', 'shruti@gmail.com', '9685741235', 1, '2003-06-14', 'CSE', '', '', 'Nagaon', '93.38', '93.20', '82.27', '', 'uploads/2223010110_KIT Resume_Shruti Pote.pdf', 'BE', ''),
(3, '2223010165', 'prerana shete', 'preranashete2004@gmail.com', '+180806151', 0, '', 'cse', 'java', 'developer', 'nagaon', '95', '100', '100', '90', 'uploads/OS (1).pdf', 'b.tech', ''),
(7, '2147483647', 'dipika bharama halun', 'Dipikahalunde@gmail.com', '2147483647', 0, NULL, NULL, NULL, NULL, NULL, NULL, NULL, NULL, NULL, NULL, NULL, 'pass'),
(9, '2122010140', 'Preeti Khade', 'preeti@gmail.com', '1854872854', 1, NULL, NULL, NULL, NULL, NULL, NULL, NULL, NULL, NULL, NULL, NULL, ''),
(11, '2223010166', 'jiya', 'jiya@gmail.com', '4787856872', 0, NULL, NULL, NULL, NULL, NULL, NULL, NULL, NULL, NULL, NULL, NULL, 'pass'),
(12, '2223010038', 'PRerama', 'Preranashete2004@gmail.com', '34567890-', 1, '27-07-2004', 'btech', 'erty', 'ertrtyhbgvc', 'erfvcdx', '20', '40', NULL, NULL, NULL, NULL, 'pass');

-- --------------------------------------------------------

--
-- Table structure for table `student`
--

DROP TABLE IF EXISTS `student`;
CREATE TABLE IF NOT EXISTS `student` (
  `id` int(10) NOT NULL,
  `username` int(20) NOT NULL,
  `password` varchar(20) NOT NULL,
  PRIMARY KEY (`username`)
) ENGINE=MyISAM DEFAULT CHARSET=latin1;

--
-- Dumping data for table `student`
--

INSERT INTO `student` (`id`, `username`, `password`) VALUES
(0, 2122010110, 'shruti@01'),
(0, 2122010111, 'prerana'),
(0, 2122010112, '12345'),
(0, 2122010113, '11111111'),
(0, 2122010114, '12345678'),
(0, 2122010115, '987654321'),
(0, 2122010116, 'dipika07'),
(0, 2122010117, 'harshada@'),
(0, 2122010118, 'karunak'),
(0, 2122010119, 'Spote@14');

-- --------------------------------------------------------

--
-- Table structure for table `users`
--

DROP TABLE IF EXISTS `users`;
CREATE TABLE IF NOT EXISTS `users` (
  `id` int(11) NOT NULL,
  `username` int(255) DEFAULT NULL,
  `password` varchar(250) NOT NULL,
  PRIMARY KEY (`id`)
) ENGINE=MyISAM DEFAULT CHARSET=latin1;

--
-- Dumping data for table `users`
--

INSERT INTO `users` (`id`, `username`, `password`) VALUES
(1, 2122010110, 'changeme');
COMMIT;

/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION */;
