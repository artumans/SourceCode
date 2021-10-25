# DDL (Data Definition / Description Language)

## CREATE
<H4> membuat tabel barang </H4>

CREATE TABLE tabel_barang (kodebarang VARCHAR(100), namabarang VARCHAR(100), harga INT(10) );

<H4> membuat tabel barang </H4>

CREATE TABLE tabel_transaksi (kodefaktur VARCHAR(100), tanggal VARCHAR(100) );

<H4> membuat tabel barang </H4>

CREATE TABLE detail_barang (kodefaktur VARCHAR(100), kodebarang VARCHAR(100), qty INT(10), harga INT(10) );

## ALTER 

constraint 

ALTER TABLE `detail_barang` ADD FOREIGN KEY (`kodebarang`) REFERENCES `tabel_barang`(`kodebarang`) ON DELETE RESTRICT ON UPDATE RESTRICT;

ALTER TABLE `detail_barang` ADD FOREIGN KEY (`kodefaktur`) REFERENCES `tabel_transaksi`(`kodefaktur`) ON DELETE RESTRICT ON UPDATE RESTRICT;

ADD primary key

ALTER TABLE `tabel_transaksi` ADD PRIMARY KEY(`kodefaktur`);

Mengganti nama

ALTER TABLE `tabel_barang` CHANGE `harga` `Harga` INT(10) NULL DEFAULT NULL;

## DROP 

DROP DATABASE test:

DROP TABLE tabel_barang;

# DML (Data Manipulation Language)

## INSERT 

<H4> insert data pada tabel barang </H4> 

INSERT INTO `tabel_barang` (`no`, `kodebarang`, `namabarang`, `harga`) VALUES (NULL, `BRG01`, `Indomie goreng jumbo`, `3500`), (NULL, `BRG02`, `Indomie soto padang`, `2000`), (NULL, 'BRG03', 'Supermie gorng', '2500'), (NULL, 'BRG04', 'Supermie soto', '2000'), (NULL, 'BRG05', 'Mie boncabe pedas', '5000');

<H4> insert data pada tabel transaksi </H4> 

INSERT INTO `tabel_transaksi` (`no`, `kodefaktur`, `tanggal`) VALUES (NULL, 'KD001', '13/07/2020'), (NULL, 'KD002', '13/07/2020'), (NULL, 'KD003', '14/07/2020');

<H4> insert data detail barang </H4>

INSERT INTO `detail_barang` (`no`, `kodefaktur`, `kodebarang`, `qty`, `harga`) VALUES (NULL, 'KD001', 'BRG01', '6', '3500'), (NULL, 'KD001', 'BRG02', '6', '2000'), (NULL, 'KD002', 'BRG03', '3', '2500'), (NULL, 'KD002', 'BRG04', '5', '2000'), (NULL, 'KD003', 'BRG05', '3', '5000');

## DELETE

DELETE FROM `tabel_barang` WHERE `tabel_barang`.`no` = 7;

## UPDATE 

UPDATE `tabel_barang` SET `namabarang` = 'Indomie goreng jumbo TANBOY' WHERE `tabel_barang`.`kodebarang` = 'BRG01';


# DQL (Data Query Language)

## SELECT

SELECT * FROM `tabel_barang`;

SELECT * FROM `tabel_transaksi`;

SELECT * FROM `detail_barang`;

# DCL (Data Control Language)

## GRANT 

## REVOKE

# TCL (Transaction Control Language)

## ROLLBACK
## COMMIT
## START TRANSACTION
## BEGIN

























