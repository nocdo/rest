# curl commands on windows:

curl.exe -v --header "content-type: text/xml" --data '@request.xml' http://localhost:8080/ws -w "\n time: %{time_total}\n"
curl.exe -v --header "content-type: text/xml" --data '@requestbiggest.xml' http://localhost:8080/ws -w "\n time: %{time_total}\n"

curl.exe -X GET localhost:8080/restrpc/meals -H 'Content-type:application/json' -v -w "\n time: %{time_total}\n"
curl.exe -X GET localhost:8080/restrpc/meals/4237681a-441f-47fc-a747-8e0169bacea1 -H 'Content-type:application/json' -v -w "\n time: %{time_total}\n"
curl.exe -X GET localhost:8080/restrpc/meals/123 -H 'Content-type:application/json' -v -w "\n time: %{time_total}\n"

curl.exe -X GET localhost:8080/rest/meals -H 'Content-type:application/json' -v -w "\n time: %{time_total}\n"
curl.exe -X GET localhost:8080/rest/meals/4237681a-441f-47fc-a747-8e0169bacea1 -H 'Content-type:application/json' -v -w "\n time: %{time_total}\n"
curl.exe -X GET localhost:8080/rest/meals/123 -H 'Content-type:application/json' -v -w "\n time: %{time_total}\n"

# connection to cs kuleuven

in cmd:
cd c:\ds\ssh
pageant rsa_id_putty.ppk
plink -L 10480:mysql.student.cs.kuleuven.be:80 st.cs.kuleuven.be
ssh r0135021@borgworm.student.cs.kuleuven.be

in browser:
localhost:10480