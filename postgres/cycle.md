    do $$
    begin
    FOR i IN 0..9 LOOP
        RAISE NOTICE 'digit %',i;
    END LOOP;
    end
    $$
