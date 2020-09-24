# CNPMNC_Chatbot
# Hướng dẫn train và khởi động
    B1: Cài đặt thư viện:
        pip install rasa
    B2: Run code:
        rasa train
        (rasa run actions)
        rasa shell (chat thử với bot)
# Kết nối với fb
    B1: Cấu hình fb app
    B2: Cài đặt ngrok
    B3: khởi động rasa, bật ngrok kiểm tra kết nối
            rasa run --endpoints endpoints.yml --credentials credentials.yml
            cổng 5005 được bật
        cd tới thư mục chứa ngrok, open terminal, sử dụng lệnh:
            ./Ngrok http 5005
            copy địa chỉ Forwarding https://xxxxx.ngrok.io
    B3: Edit callback URL trong fb app thành:
            https://xxxxx.ngrok.io/webhooks/facebook/webhook
        Verify Token: botTund
    B4: test
