1. Настроить систему для работы с устройствами на Android – реальными + эмуляторами.

2. Разработать отдельный тест на getting started (onboarding screen) в приложении википедии - пройти по 4м экранам, на каждом сделать проверку

3. Добавить в config опцию context, по значению которой остальные опции конфига будут загружаться (используя библиотеку python-dotenv) из нужного файла типа .env.context. По итогу должно быть минимум три .env-файла, например: .env.local_emulator, .env.local_real, .env.bstack

4. * Если это не было сделано ранее – именно bstack_userName и bstack_accessKey считывать не из .env.bstack, а из .env.credentials или .env (соответстенно именно эти файлы должны быть в .gitignore)

5. * Если это не было сделано ранее – отрефакторить реализацию config.py на использование pydantic

    
Запуск в Browserstack: pytest -s -v --context=bstack .
