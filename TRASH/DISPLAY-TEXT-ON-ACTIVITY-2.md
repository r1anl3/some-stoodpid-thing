activity 1:
   ```java
    public void openActivity2() {
        String str = txt.getText().toString();
        Intent intent = new Intent(getApplicationContext(), MainActivity2.class);
        intent.putExtra("message_key", str);
        startActivity(intent);
    }
   ```

activity2:
   ```java
    TextView receive_message = (TextView) findViewById(R.id.received_value_id);
    Intent intent = getIntent();
    String str = intent.getStringExtra("message_key");
    receive_message.setText(str);
   ```