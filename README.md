########################################################################
#                         DecLLVM for ida v1.2                         #
#                                  Author F8LEFT                       #
#                                  2015.12.7                           #
########################################################################

������OLLVM�Կ��Ľű�����Ҫ�Լ���дѰ����ʵָ��Ĵ��룬д�����Բο�360LLVM����AliLLVM��
��Ҫ�Ǽ̳� InstructionHelp �࣬��дget_next_instruction������
get_next_instruction ����0������������ֱ�Ӱѵ�ǰpc��reg����������ļ���
���ص�ַ���������е���Ӧ�ĵ�ַ��Ȼ����������

����᲻�ϵص���get_next_instruction�������ú�Ū�����������Ӧ�ÿ���Ū�ɲ���Ľ������Ȼ��Ч�ʷ���Ͳ������
main��������
if __name__ == "__main__":
    print("============360LLVMStart=================")
    ins = C360LLVM()
    reg = ArmReg()
    dbgEng = DbgEngine(reg, ins)
    fd = open("F:/trace.log", "w+")
    dbgEng.start_run(GetRegValue("PC"), 400, fd)
    fd.close()
    del dbgEng
    del reg
    del ins
    print("============360LLVMEnd=================")

��ʼ��DbgEngine�࣬����ins�࣬Reg(x86,arm)����Ϣ,ͬʱ��log�ļ����Ϳ�������Զ����и��١�
���򽫻�ִ��ָ��������ָ�Ȼ���˳���

��Ȼ��ֻ�Ǹ�����Ʒ�����ܿ��ܻ������ƣ���ҽ��������ź��ˡ�
