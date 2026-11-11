module mod_4_up_down_counter(clk,rst,ctrl,q_up,q_down

    );
    input clk,rst,ctrl;
    output reg [1:0]q_up;
    output  reg [1:0]q_down;
    
    always@(posedge clk)
    begin 
    if(rst)
    begin
    q_up<=2'b00;
    q_down<=2'b00;
    end 
    else if(ctrl==1) begin
    q_up<= q_up+1'b1;
    end
    else if(ctrl==0)begin
    q_down<=q_down-1'b1;
    end 
    end 
endmodule
