## fine-tuning Alpaca-Lora for Dacon Competition  
Git Clone 한 Alpaca-Lora file 중, 수정한 finetune.py만 올렸습니다.  
  
  ### 수정 부분  
  1. 아래 부분 주석 처리  
    '''  
    old_state_dict = model.state_dict  
    model.state_dict = (  
        lambda self, *_, **__: get_peft_model_state_dict(  
            self, old_state_dict()  
        )  
    ).__get__(model, type(model))  
    '''
  
나머지 진행은 notebook LLM finetuning 파일 및 Alpaca-Lora Github(https://github.com/tloen/alpaca-lora) 을 참고해주세요.
