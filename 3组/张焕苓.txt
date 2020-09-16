# 1、自动化测试类型有哪些？能解决一些什么样的问题？
# ui自动化，web自动化，接口自动化，单元自动化
# 回归测试，压力测试，兼容测试，提高测试效率，提升产品质量
"""2、某电商平台web系统基础版本耗时3个月已上线，现已进入产品版本迭代过程中
，平均每周会发布一些新的功能以及少量历史优化类容。在不考虑当前人力资源的情况下，
该项目是否适合做web自动化测试并简单说明分析过程？"""
# 适合做web自动化测试，少量的历史优化：回归测试验证
# 新的功能：做功能测试测试，接口测试，
import time

from selenium import webdriver

driver = webdriver.Chrome()
# driver.get("http://tpshop-test.itheima.net/Home/user/reg.html")
# driver.find_element_by_id("username").send_keys("13811111112")
# driver.find_element_by_name("verify_code").send_keys("8888")
# driver.find_element_by_id("password").send_keys("123456")
# driver.find_element_by_id("password2").send_keys("123456")
# driver.find_element_by_name("invite").send_keys("13811111113")
# driver.find_element_by_class_name("J_btn_agree").click()

driver.get("http://tpshop-test.itheima.net/Home/User/login.html")
driver.find_element_by_id("username").send_keys("13811111112")
time.sleep(2)
driver.find_element_by_id("password").send_keys("123456")
driver.find_element_by_name("verify_code").send_keys("8888")
driver.find_element_by_class_name("J-login-submit").click()
time.sleep(5)
driver.quit()