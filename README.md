# bubble
自己做一个备忘录小清单

视频演示
https://www.bilibili.com/video/BV1asW6eHE25/?spm_id_from=333.999.0.0&vd_source=af6a4f6de547019c024ed0dd13c217f6

docker配置环境
docker run -it --network host --rm mysql mysql -h127.0.0.1 -P13306 --default-character-set=utf8mb4 -uroot -p


gorm连接MySQL
func initMySQL() (err error) {
	dsn := "root:123456@tcp(127.0.0.1:13306)/db1?charset=utf8mb4&parseTime=True&loc=Local"
	DB, err = gorm.Open("mysql", dsn)
	if err != nil {
		return
	}
	return DB.DB().Ping()
}
