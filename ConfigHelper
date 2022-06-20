package cfg

import (
	"gopkg.in/ini.v1"
	"log"
	"strings"
)

func GetConfig(section string, key string) (value string) {
	cfg, err := ini.Load("config.ini")

	if err != nil {
		log.Println(err)
		return ``
	}

	upperSection := strings.ToUpper(section)
	lowerKey := strings.ToLower(key)

	return cfg.Section(upperSection).Key(lowerKey).String()
}
