PAC Admin Menu (QBCore + ACE + NUI)

--============================
-- INTALL
--============================
1) Put this folder in resources (e.g. resources/[pac]/pac-adminmenu)
2) Ensure oxmysql is installed and started before this resource.
3) Run the SQL below once.
4) Add ACE permissions in server.cfg.
5) ensure pac-adminmenu

--============================
-- INPUT INTO SQL
--============================
CREATE TABLE IF NOT EXISTS `pac_admin_bans` (
  `id` INT NOT NULL AUTO_INCREMENT,
  `license` VARCHAR(64) NOT NULL,
  `player_name` VARCHAR(128) NULL,
  `reason` VARCHAR(255) NULL,
  `banned_by` VARCHAR(128) NULL,
  `expires_at` BIGINT NULL,
  `created_at` BIGINT NOT NULL,
  PRIMARY KEY (`id`),
  INDEX `idx_license` (`license`)
);

--============================
-- ACE ADMIN NOTES
--============================
Make sure you are an admin under your server.cfg file, otherwise this will not callout your admin status

--============================
-- COMMANDS TO OPEN ADMIN MENU
--============================
/admin & Keybind "F10"
