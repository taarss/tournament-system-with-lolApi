# Esport
USE [lolDb]
GO

SET ANSI_NULLS ON
GO

SET QUOTED_IDENTIFIER ON
GO

CREATE TABLE Tournament(
	[id] INT IDENTITY(1,1) PRIMARY KEY NOT NULL,
	[name] NVARCHAR (100) NOT NULL,
	[teamOneId] INT NOT NULL,
	[teamTwoId] INT NOT NULL,
	[judgeId] INT NOT NULL,
	[tournamentType] NVARCHAR (10)
);


CREATE TABLE Player(
	[id] INT IDENTITY(1,1) PRIMARY KEY NOT NULL,
	[name] NVARCHAR (100) NOT NULL,
	[ingameName] NVARCHAR (100) NOT NULL,
	[rank] INT NOT NULL,
	[phoneNumber] NVARCHAR (100) NOT NULL,
);



CREATE TABLE Team(
	[id] INT NOT NULL,
	[playerId] INT NOT NULL
);

CREATE TABLE Judge(
	[id] INT IDENTITY(1,1) PRIMARY KEY NOT NULL,
	[name] NVARCHAR(100) NOT NULL,
	[phoneNumber] NVARCHAR(100) NOT NULL,
	[pay] INT NOT NULL,
	[jugdeLevel] INT NOT NULL,
);

CREATE TABLE Sponser(
	[id] INT IDENTITY(1,1) PRIMARY KEY NOT NULL,
	[companyName] NVARCHAR(150) NOT NULL,
	[field] NVARCHAR(150) NOT NULL,
	[cost] INT NOT NULL,
	[playerId] INT NOT NULL

);

SET IDENTITY_INSERT [Player] ON
INSERT INTO [Player] ([id], [name], [ingameName], [rank], [phoneNumber]) VALUES(1, 'Jens INC', '3fgfg', 69696969, 343434)
SET IDENTITY_INSERT [Player] OFF
