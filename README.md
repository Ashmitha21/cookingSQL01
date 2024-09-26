# cookingSQL01
-- a murder that occurred sometime on Jan. 15, 2018
-- and that it took place in 'SQL City' 
SELECT * 
FROM crime_scene_report
WHERE type = 'murder'
AND CITY = 'SQL City'
AND date = 20180115

![WhatsApp Image 2024-09-27 at 01 17 19_9128183e](https://github.com/user-attachments/assets/9ff72942-3ce4-4e00-8576-f69fd94f5b5f)
-- 2 witnesses
--1st lives at the last house on 'northwestern Dr'. 14887
--2nd- Annabel, lives somewhere on 'franklin ave'.
SELECT*
FROM person
AND LOWER(name) LIKE '%annabel%'
LIMIT 10


SELECT p.*,ci.*
FROM drivers_license as dl
INNER JOIN person as p on dl.id = p.license_id
INNER JOIN get_fit_now_member as gf on p.id = gf.person_id
INNER JOIN get_fit_now_check_in as ci on gf.id = ci.membership_id
WHERE plate_number LIKE '%H42W%'
AND membership_status = 'gold'
AND check_in_date = 20180109
limit 10
![output 2](https://github.com/user-attachments/assets/b8502161-3416-497e-9d28-80778cbab716)
