create TABLE Admin
( adminID VARCHAR(2) not null PRIMARY KEY,
  admin_name varchar(25) not null,
  createAdmin_adminID varchar(2) not null,
  FOREIGN KEY (createAdmin_adminID) REFERENCES Admin(adminID)
  );
create table Tasks
(taskID VARCHAR(2) not null,
 title varchar (25) not null, 
 start_date Date not null,
 end_date date not null,
 owner varchar(15) not null,
 submitted_by varchar(15),
 modified_at datetime Not null,
 PRIMARY key (taskID)
  );
  
create table Users
(user_ID varchar (3) not null,
 username varchar (25) not null,
 password varchar(100) not null,
 email varchar (50) not null,
 usertype varchar(15) not null,
 primary key(user_ID)
  );
  
create TABLE CompanyContracted
( compID VARCHAR(2) not null,
  compCity varchar(25) not null,
  compType VARCHAR(30) NOT null,
  primary key (compID),
  adminID varchar(2),
  foreign key (adminID) references Admin(adminID)
  );

create table manipulate
( 
  man_taskID varchar(3) not null,
  man_user_ID varchar(3) not null,
  FOREIGN key (man_taskID) references Tasks(taskID),
  FOREIGN key (man_user_ID) references Users(user_ID)
  );
  
 create table assign
( 
  ass_taskID varchar(3) not null,
  ass_user_ID varchar(3) not null,
  FOREIGN key (ass_taskID) references Tasks(taskID),
  FOREIGN key (ass_user_ID) references Users(user_ID)
  );
 create table createEnt
( 
  cr_userID varchar(3) not null,
  cr_adminID varchar(3) not null,
  FOREIGN key (cr_userID) references Users(user_ID),
  FOREIGN key (cr_adminID) references Admin(adminID)
  );

INSERT INTO admin VALUES ('1','Rubin Aga', '1');
INSERT INTO admin VALUES ('2','Arber Aga', '1');
INSERT INTO admin VALUES ('3','Gent Haveri', '1');
INSERT INTO admin VALUES ('4', 'Mona Lisa', '3');
INSERT INTO admin VALUES ('10', 'Jimmy Timber', '10');
INSERT INTO admin VALUES ('11', 'Eric Blackwell', '10');
INSERT INTO admin VALUES ('12', 'Edie Hamer', '10');
INSERT INTO admin VALUES ('20', 'Michael Scott', '20');
INSERT INTO admin VALUES ('21', 'Daniel White', '20');
INSERT INTO admin VALUES ('22', 'Pamela Romero', '20');


INSERT INTO users VALUES ('1', 'Ervin Aga',MD5('password1'), 'ervinaga07@grekka.com', 'user');
INSERT INTO users VALUES ('2', 'Afsana Sierra',MD5('quickpass'), 'asierra@grekka.com', 'user');
INSERT INTO users VALUES ('3', 'Brandi Barron',MD5('quickpass2'), 'bsbarron@grekka.com', 'manager');
INSERT INTO users VALUES ('4', 'Seamus Gray',MD5('quickpass3'), 'sgray@grekka.com', 'user');
INSERT INTO users VALUES ('5', 'Daryl Rhodes',MD5('quickpass4'), 'drhodes@grekka.com', 'user');
INSERT INTO users VALUES ('6', 'Bethanie Mcgrath',MD5('quickpass5'), 'bmcgrath@grekka.com', 'user');
INSERT INTO users VALUES ('7', 'Keri Hooper',MD5('quickpass6'), 'khooper@grekka.com', 'user');
INSERT INTO users VALUES ('8', 'Dalton Mackay',MD5('quickpass7'), 'dmackay@grekka.com', 'user');
INSERT INTO users VALUES ('9', 'Esha Valenzuela',MD5('quickpass8'), 'evalenzuela@grekka.com', 'user');
INSERT INTO users VALUES ('10', 'Eli Ware',MD5('quickpass9'), 'eware@grekka.com', 'manager');
INSERT INTO users VALUES ('11', 'Ivie Hood',MD5('quickpass10'), 'ihood@grekka.com', 'user');
INSERT INTO users VALUES ('12', 'Nichole Pierce',MD5('quickpass11'), 'npierce@grekka.com', 'user');
INSERT INTO users VALUES ('13', 'Tyrique Ramos',MD5('quickpass12'), 'tramos@grekka.com', 'user');
INSERT INTO users VALUES ('14', 'Caleb Franco',MD5('quickpass51'), 'cfranco@grekka.com', 'user');
INSERT INTO users VALUES ('15', 'Shirley Hartman',MD5('quickpass52'), 'shartman@grekka.com', 'user');
INSERT INTO users VALUES ('16', 'Tamika Andrew',MD5('quickpass55'), 'tandrew@grekka.com', 'user');
INSERT INTO users VALUES ('17', 'Leo Parrish',MD5('quickpass56'), 'lparrish@grekka.com', 'user');
INSERT INTO users VALUES ('18', 'Ebony Duke',MD5('quickpass57'), 'eduke@grekka.com', 'user');
INSERT INTO users VALUES ('19', 'Milton Carey',MD5('quickpass58'), 'mcarey@grekka.com', 'user');
INSERT INTO users VALUES ('20', 'Wojciech Mathews',MD5('quickpass59'), 'wmathews@grekka.com', 'user');



INSERT INTO users VALUES ('21', 'Fay Baker',MD5('quickpass22'), 'fbaker@teller.com', 'manager');
INSERT INTO users VALUES ('22', 'Jonny Tillman',MD5('quickpass537'), 'jtillman@teller.com', 'manager');
INSERT INTO users VALUES ('23', 'Eloisa Crosby',MD5('quickpass577'), 'ecrosby@teller.com', 'user');
INSERT INTO users VALUES ('24', 'Melissa Paine',MD5('quickpass579'), 'mpaine@teller.com', 'user');
INSERT INTO users VALUES ('25', 'Tabitha Mcbride',MD5('quickpass597'), 'tmcbride@teller.com', 'user');
INSERT INTO users VALUES ('26', 'Malak Harrington',MD5('quickpass557'), 'mharrington@teller.com', 'user');
INSERT INTO users VALUES ('27', 'Blair Joyner',MD5('quickpass5788'), 'bjoyner@teller.com', 'user');
INSERT INTO users VALUES ('28', 'Leanna Mercado',MD5('quickpass5127'), 'lmercado@teller.com', 'user');
INSERT INTO users VALUES ('29', 'Deanne Mcdaniel',MD5('quickpass5137'), 'dmcdaniel@teller.com', 'user');
INSERT INTO users VALUES ('30', 'Hope Hobbs',MD5('quickpass5751'), 'hhobbs@teller.com', 'user');
INSERT INTO users VALUES ('31', 'Aahil Finnegan',MD5('quickpass51227'), 'afinnegan@teller.com', 'user');
INSERT INTO users VALUES ('32', 'Aayush Ibarra',MD5('quickpass5537'), 'aibarra@teller.com', 'user');
INSERT INTO users VALUES ('33', 'Pharell Mcleod',MD5('quickpass54417'), 'pmcleod@teller.com', 'user');
INSERT INTO users VALUES ('34', 'Yazmin Ahmad',MD5('quickpass553457'), 'yahmad@teller.com', 'user');


INSERT INTO users VALUES ('35', 'Hanan Melton',MD5('quickpass51117'), 'hmelton@toppoid.com', 'user');
INSERT INTO users VALUES ('36', 'Nasir Munro',MD5('quickpass512317'), 'nmunro@toppoid.com', 'user');
INSERT INTO users VALUES ('37', 'Susanna Kendall',MD5('quickpass51247'), 'skendall@toppoid.com', 'user');
INSERT INTO users VALUES ('38', 'Isobelle Boyle',MD5('quick12pass57'), 'iboyle@toppoid.com', 'user');
INSERT INTO users VALUES ('39', 'Leanne Vazquez',MD5('quic1235kpass57'), 'lvazquez@toppoid.com', 'user');
INSERT INTO users VALUES ('40', 'Uzair May',MD5('quickpas1123s57'), 'umay@toppoid.com', 'user');
INSERT INTO users VALUES ('41', 'Lily-Ann Guzman',MD5('quiw356ckpass57'), 'lguzman@toppoid.com', 'user');
INSERT INTO users VALUES ('42', 'Britany Short',MD5('quickypass57'), 'bshort@toppoid.com', 'user');
INSERT INTO users VALUES ('43', 'Blanche Crouch',MD5('quickdgfhpass57'), 'bcrouch@toppoid.com', 'user');
INSERT INTO users VALUES ('44', 'Saanvi Calvert',MD5('quick1Rpass57'), 'scalvert@toppoid.com', 'user');
INSERT INTO users VALUES ('45', 'Zander Reilly',MD5('quickp351ass57'), 'zreilly@toppoid.com', 'manager');
INSERT INTO users VALUES ('46', 'Kaitlin Duggan',MD5('qui34ckpass57'), 'kduggan@toppoid.com', 'user');
INSERT INTO users VALUES ('47', 'Mollie Franklin',MD5('qu12312516ickpass57'), 'mfranklin@toppoid.com', 'user');
INSERT INTO users VALUES ('48', 'Ralph Harding',MD5('quicGSkpass57'), 'rharding@toppoid.com', 'user');
INSERT INTO users VALUES ('49', 'Mitchel Ballard',MD5('quicCWQkpass57'), 'mballard@toppoid.com', 'user');
INSERT INTO users VALUES ('50', 'Rania Cowan',MD5('quickp235ass57'), 'rcowan@toppoid.com', 'user');
INSERT INTO users VALUES ('51', 'Huey Barrett',MD5('quickDQDpass57'), 'hbarrett@toppoid.com', 'user');
INSERT INTO users VALUES ('52', 'Miguel Wolfe',MD5('quickpDADGJass57'), 'mwolfe@toppoid.com', 'user');
INSERT INTO users VALUES ('53', 'Dion Brock',MD5('quic1256Ykpass57'), 'dbrock@toppoid.com', 'user');


INSERT INTO tasks VALUES ('1', 'Graphical User Interface Development', '2021-02-16', '2021-03-26', 'Brandi Barron', 'Leo Parrish', '2021-11-12 14:15:17');
INSERT INTO tasks VALUES ('2', 'Marketing endeavour','2021-03-22', '2021-05-09', 'Dalton Mackay', 'Tamika Andrew', '2021-05-03 15:22:00');
INSERT INTO tasks VALUES ('3', 'Fixing banking system','2021-03-01', '2021-05-12', 'Nichole Pierce', 'Caleb Franco', '2021-05-11 11:12:14');
INSERT INTO tasks VALUES ('4', 'Improving existing framework','2021-02-24', '2021-07-29', 'Daryl Rhodes', 'Milton Carey', '2021-06-30 16:18:39');
INSERT INTO tasks VALUES ('5', 'Monitoring existing engine' ,'2021-01-01', '2021-12-24', 'Ebony Duke', 'Shirley Hartman', '2021-04-11 11:12:14');
INSERT INTO tasks VALUES ('6', 'Employee Training','2021-06-25', '2021-07-25', 'Seamus Graye', 'Eli Ware', '2021-07-25 13:19:48');
INSERT INTO tasks VALUES ('7', 'Hiring process', '2021-07-25', '2021-09-29', 'Milton Carey', 'Bethanie Mcgrath', '2021-09-29 16:48:03');
INSERT INTO tasks VALUES ('8', 'New Years Party','2021-11-01', '2021-12-17', 'Tyrique Ramos', 'Wojciech Mathews', '2021-12-16 13:55:31');

INSERT INTO tasks VALUES ('9', 'New Flavour Testing','2021-04-12', '2021-06-26', 'Melissa Paine', 'Hope Hobbs', '2021-06-26 12:02:28');
INSERT INTO tasks VALUES ('10', 'Flavour Related Health Concern Monitoring','2021-01-02', '2021-12-30', 'Fay Baker', 'Jonny Tillman', '2021-12-28 18:01:26');
INSERT INTO tasks VALUES ('11', 'Marketing ventures','2021-09-09', '2021-11-23', 'Blair Joyner', 'Aahil Finnegan', '2021-11-22 12:13:14');
INSERT INTO tasks VALUES ('12', 'Water Filtration System Monitoring', '2021-02-01', '2021-10-31', 'Pharell Mcleod', 'Yazmin Ahmad', '2021-10-30 17:29:03');
INSERT INTO tasks VALUES ('13', 'Determining the best sweetener','2021-11-02', '2021-11-16', 'Deanne McDaniel', 'Leanna Mercado', '2021-11-15 14:51:57');
INSERT INTO tasks VALUES ('14', 'Replacing sugar on drinks','2021-10-17', '2021-11-19', 'Tabitha Mcbride', 'Aayush Ibarra', '2021-11-15 09:28:31');

INSERT INTO tasks VALUES ('15', 'Fix Can Seperator Machine','2021-03-12', '2021-03-18', 'Zander Reilly', 'Kaitlin Duggan', '2021-03-17 16:41:40');
INSERT INTO tasks VALUES ('16', 'Handle sanitizing for the weekend','2021-05-01', '2021-05-31', 'Nichole Pierce', 'Caleb Franco', '2021-05-29 13:39:08');
INSERT INTO tasks VALUES ('17', 'Talks about possible acquisitions','2021-06-19', '2021-09-26', 'Ralph Harding', 'Huey Barrett', '2021-08-30 15:41:14');
INSERT INTO tasks VALUES ('18', 'Seperate 25kg paper boxes from 35kg boxes','2021-10-17', '2021-11-30', 'Uzair May', 'Miguel Wolfe', '2021-11-28 15:09:17');

INSERT INTO assign VALUES ('1', '3');
INSERT INTO assign VALUES ('2', '8');
INSERT INTO assign VALUES ('3', '12');
INSERT INTO assign VALUES ('4', '5');
INSERT INTO assign VALUES ('5', '18');
INSERT INTO assign VALUES ('6', '4');
INSERT INTO assign VALUES ('7', '19');
INSERT INTO assign VALUES ('8', '13');
INSERT INTO assign VALUES ('9', '24');
INSERT INTO assign VALUES ('10', '21');
INSERT INTO assign VALUES ('11', '27');
INSERT INTO assign VALUES ('12', '33');
INSERT INTO assign VALUES ('13', '29');
INSERT INTO assign VALUES ('14', '25');
INSERT INTO assign VALUES ('15', '45');
INSERT INTO assign VALUES ('16', '48');
INSERT INTO assign VALUES ('17', '48');
INSERT INTO assign VALUES ('18', '40');

INSERT INTO manipulate VALUES ('1', '3');
INSERT INTO manipulate VALUES ('2', '8');
INSERT INTO manipulate VALUES ('3', '12');
INSERT INTO manipulate VALUES ('4', '5');
INSERT INTO manipulate VALUES ('5', '18');
INSERT INTO manipulate VALUES ('6', '4');
INSERT INTO manipulate VALUES ('7', '19');
INSERT INTO manipulate VALUES ('8', '13');
INSERT INTO manipulate VALUES ('1', '4');
INSERT INTO manipulate VALUES ('2', '5');
INSERT INTO manipulate VALUES ('3', '6');
INSERT INTO manipulate VALUES ('4', '7');
INSERT INTO manipulate VALUES ('5', '10');
INSERT INTO manipulate VALUES ('6', '10');
INSERT INTO manipulate VALUES ('7', '9');
INSERT INTO manipulate VALUES ('8', '5');




INSERT INTO manipulate VALUES ('9', '24');
INSERT INTO manipulate VALUES ('10', '21');
INSERT INTO manipulate VALUES ('11', '27');
INSERT INTO manipulate VALUES ('12', '33');
INSERT INTO manipulate VALUES ('13', '29');
INSERT INTO manipulate VALUES ('14', '25');
INSERT INTO manipulate VALUES ('9', '21');
INSERT INTO manipulate VALUES ('10', '26');
INSERT INTO manipulate VALUES ('11', '27');
INSERT INTO manipulate VALUES ('12', '38');
INSERT INTO manipulate VALUES ('13', '30');
INSERT INTO manipulate VALUES ('14', '33');
INSERT INTO manipulate VALUES ('9', '22');
INSERT INTO manipulate VALUES ('10', '28');
INSERT INTO manipulate VALUES ('11', '23');
INSERT INTO manipulate VALUES ('12', '32');
INSERT INTO manipulate VALUES ('13', '31');
INSERT INTO manipulate VALUES ('14', '31');



INSERT INTO manipulate VALUES ('15', '45');
INSERT INTO manipulate VALUES ('16', '48');
INSERT INTO manipulate VALUES ('17', '48');
INSERT INTO manipulate VALUES ('18', '40');
INSERT INTO manipulate VALUES ('15', '32');
INSERT INTO manipulate VALUES ('16', '41');
INSERT INTO manipulate VALUES ('17', '50');
INSERT INTO manipulate VALUES ('18', '52');
INSERT INTO manipulate VALUES ('15', '53');
INSERT INTO manipulate VALUES ('16', '39');
INSERT INTO manipulate VALUES ('17', '40');
INSERT INTO manipulate VALUES ('18', '47');
INSERT INTO manipulate VALUES ('15', '41');
INSERT INTO manipulate VALUES ('16', '35');
INSERT INTO manipulate VALUES ('17', '36');
INSERT INTO manipulate VALUES ('18', '35');
INSERT INTO manipulate VALUES ('15', '37');
INSERT INTO manipulate VALUES ('16', '38');
INSERT INTO manipulate VALUES ('17', '38');
INSERT INTO manipulate VALUES ('18', '39');
INSERT INTO manipulate VALUES ('15', '51');
INSERT INTO manipulate VALUES ('16', '53');
INSERT INTO manipulate VALUES ('17', '49');
INSERT INTO manipulate VALUES ('18', '35');
INSERT INTO manipulate VALUES ('15', '41');
INSERT INTO manipulate VALUES ('16', '42');
INSERT INTO manipulate VALUES ('17', '43');
INSERT INTO manipulate VALUES ('18', '44');





INSERT INTO companycontracted VALUES ('1', 'Berlin', 'Software Development Company', '1');
INSERT INTO companycontracted VALUES ('2', 'Madrid', 'Drinks Company' , '10');
INSERT INTO companycontracted VALUES ('3', 'Scranton', 'Paper Company', '20');


INSERT INTO createent VALUES ('1', '1');
INSERT INTO createent VALUES ('2', '1');
INSERT INTO createent VALUES ('3', '1');
INSERT INTO createent VALUES ('4', '1');
INSERT INTO createent VALUES ('5', '1');
INSERT INTO createent VALUES ('6', '1');
INSERT INTO createent VALUES ('7', '1');
INSERT INTO createent VALUES ('8', '1');
INSERT INTO createent VALUES ('9', '1');
INSERT INTO createent VALUES ('10', '2');
INSERT INTO createent VALUES ('11', '2');
INSERT INTO createent VALUES ('12', '2');
INSERT INTO createent VALUES ('13', '2');
INSERT INTO createent VALUES ('14', '2');
INSERT INTO createent VALUES ('15', '3');
INSERT INTO createent VALUES ('16', '3');
INSERT INTO createent VALUES ('17', '3');
INSERT INTO createent VALUES ('18', '4');
INSERT INTO createent VALUES ('19', '4');
INSERT INTO createent VALUES ('20', '4');
INSERT INTO createent VALUES ('21', '10');
INSERT INTO createent VALUES ('22', '10');
INSERT INTO createent VALUES ('23', '11');
INSERT INTO createent VALUES ('24', '10');
INSERT INTO createent VALUES ('25', '10');
INSERT INTO createent VALUES ('26', '10');
INSERT INTO createent VALUES ('27', '10');
INSERT INTO createent VALUES ('28', '10');
INSERT INTO createent VALUES ('29', '10');
INSERT INTO createent VALUES ('30', '10');
INSERT INTO createent VALUES ('31', '11');
INSERT INTO createent VALUES ('32', '11');
INSERT INTO createent VALUES ('33', '12');
INSERT INTO createent VALUES ('34', '12');
INSERT INTO createent VALUES ('35', '20');
INSERT INTO createent VALUES ('36', '20');
INSERT INTO createent VALUES ('37', '21');
INSERT INTO createent VALUES ('38', '20');
INSERT INTO createent VALUES ('39', '20');
INSERT INTO createent VALUES ('40', '20');
INSERT INTO createent VALUES ('41', '20');
INSERT INTO createent VALUES ('42', '20');
INSERT INTO createent VALUES ('43', '20');
INSERT INTO createent VALUES ('44', '20');
INSERT INTO createent VALUES ('45', '21');
INSERT INTO createent VALUES ('46', '21');
INSERT INTO createent VALUES ('47', '22');
INSERT INTO createent VALUES ('48', '22');
INSERT INTO createent VALUES ('49', '22');
INSERT INTO createent VALUES ('50', '22');
INSERT INTO createent VALUES ('51', '22');
INSERT INTO createent VALUES ('52', '22');
INSERT INTO createent VALUES ('53', '22');

SELECT T.title, T.owner, T.modified_at FROM tasks T INNER JOIN assign A ON T.taskID = A.ass_taskID INNER JOIN users U ON U.user_ID = A.ass_user_ID WHERE email LIKE '%grekka%'; 

SELECT U.user_ID, U.username FROM users U INNER JOIN assign A ON U.user_ID = A.ass_user_ID WHERE email LIKE '%teller%'; 

SELECT taskID, title, start_date, end_date, owner FROM tasks WHERE start_date > '2021/06/01'; 

SELECT T.title, T.owner FROM tasks T WHERE T.end_date > DATE_ADD(T.modified_at, INTERVAL 20 DAY); 

SELECT T.taskID, T.title FROM tasks T INNER JOIN manipulate M ON M.man_taskID = T.taskID INNER JOIN users U ON U.user_ID = M.man_user_ID WHERE username='Fay Baker';

SELECT A.adminID, A.admin_name FROM admin A, companycontracted C WHERE C.adminID = A.createAdmin_adminID AND C.adminID <> A.adminID; 

SELECT M.man_user_ID, COUNT(M.man_user_ID) AS most_done FROM manipulate M GROUP BY M.man_user_ID ORDER BY most_done DESC LIMIT 5; 

SELECT T.title, U.user_ID, U.username FROM users U INNER JOIN manipulate M ON M.man_user_ID = U.user_ID INNER JOIN tasks T ON T.taskID = M.man_taskID WHERE U.usertype = 'manager' AND U.email LIKE '%teller%';

SELECT T.taskID, T.modified_at FROM tasks T WHERE DATEDIFF(CURDATE(),T.modified_at) < 1; 

SELECT * FROM users WHERE user_ID NOT IN (SELECT man_user_ID FROM manipulate); 
